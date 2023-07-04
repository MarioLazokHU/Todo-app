<script>
  export let todo;
  export let remove;

  function toggleTodo() {
    todo.completed = !todo.completed;
  }

  function deleteTodo() {
    remove(todo.id);
  }
</script>

<div class="todo-item">
  <input type="checkbox" bind:checked={todo.completed} on:change={toggleTodo} />
  <span class:completed={todo.completed}>{todo.text}</span>
  <button on:click={deleteTodo}>Delete</button>
</div>

<style>
  .todo-item {
    margin-bottom: 8px;
  }
</style>

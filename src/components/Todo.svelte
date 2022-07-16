<script>
    import { deletTodo, toggleTodoCompleted } from "../stores/todoStore";
    export let todo;
</script>

<li class="bg-white flex items-center shadow-sm border border-gray-200 rounded-lg my-2 py-2 p´x-4">
    <input 
        name="completed" 
        type='checkbox' 
        checked={todo.completed} 
        on:change={() => toggleTodoCompleted(todo.id)}
        class="mr-2 form-checkbox h-5 w-5"
        />
        <span class={`flex-1 text-gray-800 ${todo.completed ? 'line-through': ''}`}>{todo.text}</span>
        <button class="textsm bg-red-500 hover:bg-red-600 text-white py-1 px-2 focus:outline-none focus:shadow-outline" on:click={() => deletTodo(todo.id)}>Delete</button>
</li>
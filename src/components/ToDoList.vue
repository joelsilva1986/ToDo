<template>
    <div>
        <h1> To-Do List</h1>
        <input v-model.trim="task"
            type="text"
            placeholder="Adicionar novo To-Do"
            >
        <button @click="addTask" type="button">Adicionar</button>
        <ul>
            <li v-for="task in tasks" :key="task">{{ task }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "ToDoList",
    data() {
        return {
            task: "",
            tasks: []
        }
    },
    methods: {
        addTask() {
            this.tasks.push(this.task)
            this.task=""
        }
    }
}
</script>

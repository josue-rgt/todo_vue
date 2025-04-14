<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form class="row" @submit.prevent="props.cadastraTarefa">
        <div class="col">
            <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required
                type="text" placeholder="Digite a descrição da tarefa" class="form-control">
        </div>
        <div class="col-md-2">
            <button class="btn btn-primary" type="submit">Cadastrar</button>
        </div>
        <div class="col-md-2">
            <select @change="props.trocarFiltro" class="form-control">
                <option value="todas">Todas tarefas</option>
                <option value="pendentes">Pendentes</option>
                <option value="finalizadas">Finalizadas</option>
            </select>
        </div>
    </form>
</template>
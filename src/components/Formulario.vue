<script setup>
const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp']);
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" class="form-control" type="text"
                    placeholder="Digite a descrição da tarefa" required>
            </div>

            <div class="col-md-2">
                <button type="submit" class="btn btn-primary">Cadastrar</button>
            </div>

            <div class="col-md-2">
                <select @change="props.trocarFiltro" class="form-select">
                    <option value="todas">Todas as tarefas</option>
                    <option value="pendentes">Tarefas pendentes</option>
                    <option value="finalizadas">Tarefas finalizadas</option>
                </select>
            </div>

        </div>
    </form>
</template>
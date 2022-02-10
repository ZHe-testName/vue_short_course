<template>
    <!-- В секции template мы описываем наши шаблоны
    и всю разметку -->
    <div>
        <div>
            <!-- слушатели собитий привязываются к элементам с помощю дирректив -->
            <!-- диррективу v-on можно заменить на знак собаки @ это более короткая запись -->
            <button @click="addLike">Like</button>
            <button @click="addDislike">Dislike</button>
        </div>

        <!-- С помощю интерполяции мы можем обращаться к данным из моделей -->
        <div>Количество лайков : <strong>{{likes}}</strong> </div>
        <div>Количество дизлайков : <strong>{{dislikes}}</strong> </div>
    </div>
</template>

<script>
// В секции script мы описываем всю логику и остальное
// по сути это и есть наш компонент

// Секция по дефолту должна возвращать объект в котором и 
// будут наши модели
export default {
    data() {
        return {
            likes: 0,
            dislikes: 0,
        };
    },
    // Функции описываются в поле methods
    methods: {
        //для обращения к данным из data используем this
        addLike() {
            this.likes += 1;
        },
        addDislike() {
            this.dislikes += 1;
        },
    },
}
</script>

<style>

</style>
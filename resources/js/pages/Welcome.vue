<script setup lang="ts">
import { Head, Link } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Добро пожаловать"></Head>

    <div class="flex min-h-screen flex-col bg-black text-gray-900">
        <!-- Навигация (перенесена наверх) -->
        <nav class="bg-black text-white p-4 shadow-md">
            <div class="max-w-full flex justify-between items-center">
                <div>

                </div>
                <div class="flex gap-6">
                    <template v-if="$page.props.auth.user">
                        <Link
                            :href="route('dashboard')"
                            class="hover:text-gray-300 transition duration-200"
                        >
                            Dashboard
                        </Link>
                    </template>

                    <template v-else>
                        <Link
                            :href="route('login')"
                            class="hover:text-gray-300 transition duration-200"
                        >
                            Войти
                        </Link>
                        <Link
                            :href="route('register')"
                            class="hover:text-gray-300 transition duration-200"
                        >
                            Регистрация
                        </Link>
                    </template>
                </div>
            </div>
        </nav>

        <div class="flex-1 flex flex-col justify-center items-center p-8 bg-black text-white">
            <h1 class="text-4xl font-bold mb-6 text-center lg:text-left">
                Панель администратора для музыкальной платформы
            </h1>

            <p class="text-lg mb-12 text-center lg:text-left max-w-3xl">
                Добро пожаловать! Управляйте платформой, следите за активностью пользователей, публикуйте курсы и анализируйте результаты — все в одном месте. Мы создали мощный инструментарий для оптимизации вашего контента и повышения вовлеченности.
            </p>

            <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3 w-full max-w-6xl">
                <!-- Карточка контента -->
                <div class="rounded-2xl border border-transparent bg-gray-900 p-8 shadow-lg hover:shadow-2xl transition duration-300 ease-in-out transform hover:scale-105">
                    <h3 class="text-xl font-semibold mb-2">Управление контентом</h3>
                    <p class="text-sm">
                        Добавляйте и редактируйте обучающие курсы, аудио и видео. Следите за качеством материалов на платформе. Убедитесь, что контент соответствует стандартам качества и интересен вашей аудитории.
                    </p>
                </div>

                <div class="rounded-2xl border border-transparent bg-gray-900 p-8 shadow-lg hover:shadow-2xl transition duration-300 ease-in-out transform hover:scale-105">
                    <h3 class="text-xl font-semibold mb-2">Управление участниками</h3>
                    <p class="text-sm">
                        Модерируйте профили пользователей, настраивайте роли и доступ, следите за вовлечённостью. Управляйте активностью участников и создавайте персонализированные предложения для повышения их интереса.
                    </p>
                </div>

                <div class="rounded-2xl border border-transparent bg-gray-900 p-8 shadow-lg hover:shadow-2xl transition duration-300 ease-in-out transform hover:scale-105">
                    <h3 class="text-xl font-semibold mb-2">Управление контентом</h3>
                    <p class="text-sm">
                        Добавляйте и редактируйте обучающие курсы, аудио и видео. Следите за качеством материалов на платформе. Убедитесь, что контент соответствует стандартам качества и интересен вашей аудитории.
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
/* Добавление стилей для навигации */
nav {
    position: sticky;
    top: 0;
    z-index: 10;
}

nav a {
    text-decoration: none;
}
</style>

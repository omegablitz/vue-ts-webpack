<template>
    <div>
        <div class="greeting">Hello {{ exclamationMarks }}</div>
        <button @click="decrement">
            -
        </button>
        <button @click="increment">
            +
        </button>
    </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

@Component
export default class App extends Vue {
    // initial data
    enthusiam = 5;

    // computed
    get exclamationMarks(): string {
        return Array(this.enthusiam + 1).join('!');
    }

    // methods
    increment(): void {
        this.enthusiam++;
    }
    decrement(): void {
        this.enthusiam--;
    }
}
</script>

<style>
.greeting {
    font-size: 20px;
}
</style>

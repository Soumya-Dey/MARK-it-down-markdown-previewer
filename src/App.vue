<template>
    <div id="app">
        <nav class="navbar">
            <div class="logo"><span>#MARK</span> it-down</div>
            <a href="https://github.com/Soumya-Dey" target="_blank"
                ><i class="fab fa-github"></i> github</a
            >
        </nav>

        <div class="container">
            <div class="md-text">
                <h2>Markdown</h2>
                <textarea
                    class="md-textarea"
                    v-model="text"
                    placeholder="Type your markdown here..."
                ></textarea>
            </div>
            <div class="formatted-text">
                <h2>Formatted Text</h2>
                <vue-markdown class="formatted-textarea" :source="text"
                    >Formatted text will appear here...</vue-markdown
                >
            </div>
        </div>
    </div>
</template>

<script>
import VueMarkdown from "vue-markdown";

export default {
    name: "App",
    components: {
        VueMarkdown,
    },
    data() {
        return {
            text: "",
        };
    },
};
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: #ffeaa7;
    font-family: "Montserrat", sans-serif;
    font-weight: 500;
    line-height: 1.4;
}

.navbar {
    background-color: #fff;
    padding: 0.8em 2em;
    margin: 1.4em 3em;
    color: #202020;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border: 2px solid #4fc08d;
    border-radius: 12px;
    box-shadow: 6px 6px 0 0 #4fc08d;
}

.logo {
    font-weight: 700;
}

.logo span {
    color: #4fc08d;
    font-size: 1.4em;
    font-weight: 700;
}

.navbar a {
    text-decoration: none;
    color: #202020;
}

.navbar a:hover {
    color: #4fc08d;
}

.fa-github {
    font-size: 1.2em;
    margin-right: 2px;
}

.container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4em;
    margin: 1.4em 3em;
}

.md-text,
.formatted-text {
    width: 100%;
}

h2 {
    margin: 1em 0 0.8em 1.2em;
}

.md-textarea,
.formatted-textarea {
    width: 100%;
    height: 400px;
    outline: none;
    border: 1px solid #ddd;
    background-color: #fff;
    box-shadow: 6px 6px 0 0 #4fc08d;
    border: 2px solid #4fc08d;
    border-radius: 12px;
    padding: 1.4em 1.6em;
    transition: all 0.2s ease;
}

.md-textarea {
    font-size: 1.2em;
}

.md-textarea:focus {
    border-color: #35495e;
    transform: translate(-4px, -4px);
    box-shadow: 6px 6px 0 0 #35495e, 12px 12px 0 0 #35495e;
}
</style>

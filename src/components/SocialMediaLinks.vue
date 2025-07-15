<template>
    <div class="container">
        <h3 class="title">{{ title }}</h3>
        <p class="description">{{ description }}</p>
        <div class="links-display">
            <div class="social-link-container">
                <a class="social-link" href="http://www.github.com/nicolasanunes" target="_blank" rel="noopener noreferrer">
                    <fa-icon icon="fa-brands fa-2xl fa-github" />
                </a>
                <a class="social-link" href="https://instagram.com/nan.jsdev" target="_blank" rel="noopener noreferrer">
                    <fa-icon icon="fa-brands fa-instagram" />
                </a>
                <a class="social-link" href="https://www.linkedin.com/in/nicolasanunes" target="_blank" rel="noopener noreferrer">
                    <fa-icon icon="fa-brands fa-linkedin" />
                </a>
                <a class="social-link" href="https://web.whatsapp.com/send?phone=34999514231" target="_blank" rel="noopener noreferrer">
                    <fa-icon icon="fa-brands fa-lg fa-whatsapp" />
                </a>
            </div>
        </div>
        <h3 class="subtitle">Learn More</h3>
        <div class="link-container">
            <LinkComponent image="/logo.png" title="New Idea or Project? Contact me 💡" url="https://web.whatsapp.com/send?phone=34999514231" />
        </div>
        <h3 class="subtitle">Portfolio Projects</h3>
        <div class="link-container">
            <LinkComponent image="/canalvos-logo.png" title="Canal VOS" url="https://canalvos.com.br/" />
            <LinkComponent image="/chcd-logo.png" title="Caring Hearts Christian Daycare" url="https://caringheartssf.com/" />
        </div>
    </div>
</template>

<script>
import LinkComponent from './LinkComponent.vue';

export default {
    name: 'SocialMediaLinks',
    props: {
        title: String,
        description: String
    },
    components: {
        LinkComponent
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
    margin: 40px 0 0;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    display: inline-block;
    margin: 0 10px;
}
.container {
    display: flex;
    flex-direction: column;
}

.social-link-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 1.25rem;
    width: 100%;
}

.social-link {
    font-size: 2em;
}

.social-link:hover {
    transform: scale(1.1);
}

.link-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
</style>

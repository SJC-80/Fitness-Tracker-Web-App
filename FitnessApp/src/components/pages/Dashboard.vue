<script setup>
    import { gymHealthFacts } from '../../utils'
    import Grid from '../Grid.vue'
    console.log(gymHealthFacts)
    const randomNumber = Math.floor(Math.random() * gymHealthFacts.length)
    const FactofTheDay = gymHealthFacts[randomNumber]
    console.log(FactofTheDay)
</script>

<template>
    <section id="dahsboard">
        <div class="card tip-container">
            <h2>Welcome Smoldier</h2>
            <div>
                <p class="tip"><strong>Daily Tip</strong><br/>{{ FactofTheDay }} </p>
            </div>
            <button>Start workout &rarr;</button>
        </div>
        <Grid/>
    </section>
</template>

<style scoped>
    .tip-container,
    .tip-container div,
    #dashboard {
        display: flex;
    }

    .tip-container,
    #dashboard {
        flex-direction: column;
    }

    #dashboard {
        gap: 2rem;
    }    

    .tip-container {
        gap: 0.5rem;
    }

    @media (min-width: 640px){
        .tip-container{
            gap: 1rem;
        }
    }
</style>
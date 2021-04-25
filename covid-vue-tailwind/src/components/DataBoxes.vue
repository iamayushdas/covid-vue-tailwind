<template>
    <div class="grid md:grid-cols-2 gap-4">
        <div class="shadow-md bg-green-100 p-10 text-center rounded">
            <h3 class="text-3xl text-green-900 font-bold mb-4">Recovered</h3>

            <div class="text-2xl mb-4">
                <span class="font-bold">
                    New:
                </span>
                {{ numberWithCommas(stats.NewRecovered) }}
            </div>
            <div class="text-2xl mb-4">
                <span class="font-bold">
                    Total:
                </span>
                {{ numberWithCommas(stats.TotalRecovered) }}
            </div>
        </div>
        <div class="shadow-md bg-blue-100 p-10 text-center rounded">
            <h3 class="text-3xl text-blue-900 font-bold mb-4">cases</h3>

            <div class="text-2xl mb-4">
                <span class="font-bold">
                    New:
                </span>
                {{ numberWithCommas(stats.NewConfirmed) }}
            </div>
            <div class="text-2xl mb-4">
                <span class="font-bold">
                    Total:
                </span>
                {{ numberWithCommas(stats.TotalConfirmed) }}
            </div>
        </div>

        <div class="shadow-md bg-red-200 p-10 text-center rounded">
            <h3 class="text-3xl text-red-900 font-bold mb-4">Deceased</h3>

            <div class="text-2xl mb-4">
                <span class="font-bold">
                    New:
                </span>
                {{ numberWithCommas(stats.NewDeaths) }}
            </div>
            <div class="text-2xl mb-4">
                <span class="font-bold">
                    Total:
                </span>
                {{ numberWithCommas(stats.TotalDeaths) }}
            </div>
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'dataBoxes',
    props: ['stats'],
    methods: {
        numberWithCommas(x) {
            return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',')
        }
    }

}
</script>
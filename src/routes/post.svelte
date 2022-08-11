<script context="module">
    /**
     * @type {import('./__types/post').Load}
     */
    export async function load(load) {
        const res = await load.fetch('https://jsonplaceholder.typicode.com/todos/1');
        
        return {
            props: {
                data: await res.json()
            }
        }
    }
</script>

<script>
    /**@type {any}*/
    export let data;
</script>

{JSON.stringify(data)}
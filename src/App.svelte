<script lang="ts">
    import Toast from './components/Toast.svelte'
    export let name: string;

    let visable: boolean = false;

    let userLogin = document.querySelector('meta[name="user-login"]')?.getAttribute('content');
    if(userLogin) name = userLogin;
    
    setTimeout(() => visable = true, 1000);

</script>

<Toast bind:visable>
    <div class="body">
        <strong>Hello, {name}!</strong><br>
        Do good things ❤️
    </div>
</Toast>

<style>
    .body {
        text-align: center;
    }
</style>
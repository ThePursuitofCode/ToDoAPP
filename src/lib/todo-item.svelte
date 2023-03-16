<div class="todo done">
    <form action="" method="" >
        <input type="hidden" name="done" value="" />
        <button class="toggle" aria-label="Mark Done / Not Done"></button>
    </form>

    <form action="" method="" class="text">
        <input type="text" />
        <button class="save" aria-label="Save todo"></button>
    </form>

    <form action="" method="">
        <button class="delete" aria-label="Delete todo"></button>
    </form>
</div>

<style>
    .todo {
        display: grid;
        grid-template-columns: 2rem 1fr 2rem;
        grid-gap: 0.5rem;
        align-items: center;
        margin: 0 0 0.5rem 0;
        padding: 0.5rem;
        background-color: white;
        border-radius: 8px;
        filter: drop-shadow(2px 4px 6px rgba(0,0,0,0,0.1));
        transform: translate(-1px, -1px);
        transition: filter 0.2s, transform 0.2s;
    }

    .todo button {
        width: 2em;
        height: 2em;
        border: none;
        background-color: transparent;
        background-position: 50% 50%;
        background-repeat: no-repeat;
    }

    .todo input {
       flex: 1; 
       padding: 0.5em 2em 0.5em 0.8em;
       border-radius: 3px;
    }

    button.toggle {
        border: 1px solid rgba(0,0,0,0.2);
        border-radius: 50%;
        box-sizing: border-box;
        background-size: 1em auto;
    }

    .text {
        position: relative;
        display: flex;
        align-items: center;
        flex: 1;
    }

    .save {
        position: absolute;
        right: 0;
        opacity: 0;
        background-image: url("data:image/svg+xml,%3Csvg width='24px' height='24px' stroke-width='1.5' viewBox='0 0 24 24' fill='none' xmlns='http://www.w3.org/2000/svg' color='%23000000'%3E<path d='M3 7.5V5a2 2 0 012-2h11.172a2 2 0 011.414.586l2.828 2.828A2 2 0 0121 7.828V19a2 2 0 01-2 2H5a2 2 0 01-2-2v-2.5M6 21v-4' stroke='%23000000' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'%3E%3C/path%3E<path d='M18 21v-7.4a.6.6 0 00-.6-.6H15M16 3v5.4a.6.6 0 01-.6.6h-1.9M8 3v3M1 12h11m0 0L9 9m3 3l-3 3' stroke='%23000000' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'%3E%3C/path%3E%3C/svg%3E");

    }

    .todo input:focus + .save,
    .save:focus {
        transition: opacity 0.2s;
        opacity: 1;
        cursor: pointer;
    }

    .delete {
        background-image: url("data:image/svg+xml,%3Csvg width='24px' height='24px' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M9.172 14.828L12.001 12m2.828-2.828L12.001 12m0 0L9.172 9.172M12.001 12l2.828 2.828M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10z' fill='none' stroke='%23000000' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E");
        opacity: 0.2;
    }

    .delete:hover,
    .delete:focus {
        transition: opacity 0.2s;
        opacity: 1;
        cursor: pointer;
    }
    /* TODO: Uncomment when API endpoints are available.
    .done {
        transform: none;
        opacity: 0.4;
        filter: drop-shadow(0px 0px 1px rgba(0, 0, 0, 0.1));
    }

    .done .toggle {
        background-image: url("data:image/svg+xml,%3Csvg width='22' height='16' viewBox='0 0 22 16' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M20.5 1.5L7.4375 14.5L1.5 8.5909' stroke='%23676778' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E");
    } */
</style>
<script lang="ts">
import FeedBackItem from "./FeedBackItem.svelte";
import { fade, scale } from "svelte/transition";
import { FeedbackStore } from '../stores';
</script>

{#each $FeedbackStore as item (item.id)}
    <div in:scale out:fade>
        <FeedBackItem {item} />
    </div>
{/each}
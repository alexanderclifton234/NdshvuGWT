<template>
    <span>{{ displayText }}</span>
</template>

<script>
export default {
    props: {
        value: {
            type: String,
            default: null,
        },
        /** Should only the date be displayed? */
        dateOnly: {
            type: Boolean,
            default: false,
        },
    },

    computed: {
        displayText() {
                return this.$root.date(this.value);
            } else {
                return this.$root.datetime(this.value);
            }
        },
    },
};
</script>

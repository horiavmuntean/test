<script>
  import "@vaadin/confirm-dialog";
  import "@vaadin/button";
  import "@vaadin/date-picker";

  let open = false;
</script>

<vaadin-confirm-dialog
  header="Header"
  cancel
  on:cancel={(e) => console.log(e)}
  confirm-text="OK"
  on:confirm={(e) => console.log(e)}
  opened={open}
  on:opened-changed={(e) => (open = e.detail.value)}
>
<vaadin-date-picker
label="Settlement Date"
style="width: 100%;"
/>
</vaadin-confirm-dialog>

<vaadin-button on:click={() => (open = true)}>Open</vaadin-button>
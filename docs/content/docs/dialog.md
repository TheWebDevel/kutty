---
title: Dialog
---

## Basic

{{< code html >}}
<button class="btn btn-primary" @click="$dispatch('show-modal')" x-on:keydown.escape="$dispatch('hide-modal')" aria-haspopup="dialog">Open Dialog</button>

<div class="dialog" x-data="dialog()" x-spread="dialog" x-cloak @show-modal.window="show" @hide-modal.window="close" x-data="{open: false}" x-init="initDialog($el)">
  <div class="dialog-content">
    <div class="dialog-header">Dialog Title
      <button type="button" class="btn btn-light btn-sm btn-icon" aria-label="Close" @click="close"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="18" y1="6" x2="6" y2="18"></line><line x1="6" y1="6" x2="18" y2="18"></line></svg></button>
    </div>
    <div class="dialog-body">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam eius fugiat illum repudiandae commodi inventore magnam unde vero cupiditate molestiae?</div>
    <div class="dialog-footer">
      <button type="button" class="btn btn-light" @click="close">Close</button>
      <button type="button" class="btn btn-primary">Save changes</button>
    </div>
  </div>
</div>
{{< /code >}}

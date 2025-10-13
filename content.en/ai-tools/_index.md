---
title: "AI Tools"
weight: 80
---
# Introduction {anchor=false}
Here you will learn about AI tools!

# Upscale
Upscaling is required for most photos you find online. From art to cards it all needs to be a high resolution by the time you print. You will need an upscaling software and a safetensors file.

## Upscale software
- **chaiNNer** [{{< badge style="info" title="Github" >}}](https://github.com/chaiNNer-org/chaiNNer) is a stand-alone upscaling GUI. You can use templates [{{< badge style="info" title="Github" >}}](https://github.com/Kim2091/chaiNNer-Templates) to get started.
- **ComfyUI** [{{< badge style="info" title="Github" >}}](https://github.com/comfyanonymous/ComfyUI) is a modular diffusion model GUI, api and backend with a graph/nodes interface. You can upscale and [remove text](/ai-tools/#remove-text) with this.

## Safetensors file
**OpenModelDB** [{{< badge style="info" title="Website" >}}](https://openmodeldb.info/) has many custom upscaling models. An interactive visual comparison of upscaling models [{{< badge style="info" title="Website" >}}](https://phhofm.github.io/upscale/favorites.html) is available.
- **Real-ESGRAN-x4plus** [{{< badge style="info" title="Hugging Face" >}}](https://huggingface.co/Comfy-Org/Real-ESRGAN_repackaged/blob/main/RealESRGAN_x4plus.safetensors)
- **4x-UltraSharpV2** [{{< badge style="info" title="Github" >}}](https://github.com/Kim2091/Kim2091-Models/releases/tag/4x-UltraSharpV2) by Kim2091 [{{< badge style="info" title="Ko-fi" >}}](https://ko-fi.com/J3J3BCC3L)

# Remove text
If you need to translate a card to your native language, you have to remove the original language text from the card. Use a **FLUX.1-Kontext-Dev** template [{{< badge style="info" title="Website" >}}](https://nunchaku.tech/docs/ComfyUI-nunchaku/workflows/kontext.html#nunchaku-flux-1-kontext-dev-json) to modify the original card photo, then [upscale](/ai-tools/#upscale). You can integrate upscaling directly into the pipeline of text removal using ComfyUI.

## Safetensors file
- **FLUX.1-Kontext-Dev** [{{< badge style="info" title="Hugging Face" >}}](https://huggingface.co/Comfy-Org/flux1-kontext-dev_ComfyUI/blob/main/split_files/diffusion_models/flux1-dev-kontext_fp8_scaled.safetensors) - 12GB file size
  > [!WARNING]
  > **Warning**  
  > Requires 16-20GB of VRAM
  - Latest Image-to-Image diffusion model from **Black Forest Labs** [{{< badge style="info" title="Hugging Face" >}}](https://huggingface.co/black-forest-labs)
  - If you want to test this before downloading you can try the live demo [{{< badge style="info" title="Hugging Face" >}}](https://huggingface.co/spaces/black-forest-labs/FLUX.1-Kontext-Dev)
  - Model source available on [{{< badge style="info" title="Github" >}}](https://github.com/black-forest-labs/flux)
- **Nunchaku-FLUX.1-Kontext-Dev** [{{< badge style="info" title="Hugging Face" >}}](https://huggingface.co/nunchaku-tech/nunchaku-flux.1-kontext-dev) - 7GB file size
  > [!WARNING]
  > **Warning**  
  > Requires 8-12GB of VRAM
  - 4-bit version of FLUX.1-Kontext-Dev from **MIT hanlab** [{{< badge style="info" title="Website" >}}](https://hanlab.mit.edu)
  - Different safetensors files for users with *non-Blackwell GPUs (<=40-series)* [{{< badge style="info" title="Hugging Face" >}}](https://huggingface.co/nunchaku-tech/nunchaku-flux.1-kontext-dev/blob/main/svdq-int4_r32-flux.1-kontext-dev.safetensors) and for users with *Blackwell GPUs (50-series)* [{{< badge style="info" title="Hugging Face" >}}](https://huggingface.co/nunchaku-tech/nunchaku-flux.1-kontext-dev/blob/main/svdq-fp4_r32-flux.1-kontext-dev.safetensors)
  - See ComfyUI-nunchaku [{{< badge style="info" title="Github" >}}](https://github.com/nunchaku-tech/ComfyUI-nunchaku) for ComfyUI setup
  - Model source available on [{{< badge style="info" title="Github" >}}](https://github.com/nunchaku-tech/nunchaku)
  
## Prompt example
Remove the "sample" text in the center. Remove the text at the top. Remove all card text at the bottom. Keep the top left numbers. Remove all card text at the bottom.
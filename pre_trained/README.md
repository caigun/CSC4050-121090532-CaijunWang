## FACodec pre-trained model
For the pre-trained FACodec Models, you can download the checkpoint from Amphion:

```
https://huggingface.co/amphion/naturalspeech3_facodec
```

Or use the built-in library to download:

```python
from huggingface_hub import hf_hub_download

encoder_ckpt = hf_hub_download(repo_id="amphion/naturalspeech3_facodec", filename="ns3_facodec_encoder.bin")
decoder_ckpt = hf_hub_download(repo_id="amphion/naturalspeech3_facodec", filename="ns3_facodec_decoder.bin")

fa_encoder.load_state_dict(torch.load(encoder_ckpt))
fa_decoder.load_state_dict(torch.load(decoder_ckpt))

# for redecoder
redecoder_ckpt = hf_hub_download(repo_id="amphion/naturalspeech3_facodec", filename="ns3_facodec_redecoder.bin")
fa_redecoder.load_state_dict(torch.load(redecoder_ckpt))
```
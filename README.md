# CREST Dictation: modellen

Spraakmodellen die de macOS-app CREST Dictation op verzoek downloadt. De app zelf bevat geen modellen; hij haalt ze hier op en controleert elk bestand op grootte en SHA256 voordat hij het gebruikt.

## Juvoly-fyNL-FRIS-withCV, int8 ONNX (Frysk)

Release: `juvoly-fynl-fris-cv-int8-v1`

| Bestand | Bytes | SHA256 |
|---|---|---|
| `encoder-model.int8.onnx` | 654663660 | `755d00311c3cae4897e2f7787ea96c5e9bf38fe18947b754e63fd30dc2fc83ea` |
| `decoder_joint-model.int8.onnx` | 18202004 | `c4d6ced1cb0bc0899a684e7bdef4c430d4756da7cb0976b6720f81a352a53e05` |
| `nemo128.onnx` | 139764 | `a9fde1486ebfcc08f328d75ad4610c67835fea58c73ba57e3209a6f6cf019e9f` |
| `vocab.txt` | 93939 | `d58544679ea4bc6ac563d1f545eb7d474bd6cfa467f0a6e2c1dc1c7d37e3c35d` |

### Herkomst en naamsvermelding

- **Model:** Juvoly-fyNL-FRIS-withCV by Juvoly, a fine-tune of NVIDIA Parakeet TDT 0.6B v3 (CC BY 4.0).
- **Data:** Provinsje Fryslân, Taalstudio Prins and Juvoly, via [huggingface.co/datasets/Juvoly/Frisian-dialogue](https://huggingface.co/datasets/Juvoly/Frisian-dialogue). Licensed under CC BY-SA 4.0.
- **Wat wij hebben veranderd:** Growth Dept heeft het originele `.nemo`-model omgezet naar ONNX, met gedeeltelijke int8-kwantisatie (de depthwise-convoluties zijn in fp32 gebleven). De gewichten zijn verder niet hertraind.
- `nemo128.onnx` en `vocab.txt` zijn byte voor byte gelijk aan de bestanden van NVIDIA Parakeet TDT 0.6B v3 in ONNX-vorm door istupakov ([istupakov/parakeet-tdt-0.6b-v3-onnx](https://huggingface.co/istupakov/parakeet-tdt-0.6b-v3-onnx), CC BY 4.0).

### Licentie

Deze aangepaste versie valt onder de **Creative Commons Attribution-ShareAlike 4.0 International**-licentie (CC BY-SA 4.0), zie [LICENSE](LICENSE) en https://creativecommons.org/licenses/by-sa/4.0/.

Er worden geen garanties gegeven. Zie de licentie voor de volledige voorwaarden.

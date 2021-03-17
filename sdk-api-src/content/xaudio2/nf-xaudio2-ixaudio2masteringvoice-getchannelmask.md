---
UID: NF:xaudio2.IXAudio2MasteringVoice.GetChannelMask
title: IXAudio2MasteringVoice::GetChannelMask (xaudio2.h)
description: Returns the channel mask for this voice.
helpviewer_keywords: ["GetChannelMask","GetChannelMask method [XAudio2 Audio Mixing APIs]","GetChannelMask method [XAudio2 Audio Mixing APIs]","IXAudio2MasteringVoice interface","IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs]","GetChannelMask method","IXAudio2MasteringVoice.GetChannelMask","IXAudio2MasteringVoice::GetChannelMask","xaudio2.ixaudio2masteringvoice_interface_getchannelmask","xaudio2/IXAudio2MasteringVoice::GetChannelMask"]
old-location: xaudio2\ixaudio2masteringvoice_interface_getchannelmask.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2masteringvoice.IXAudio2MasteringVoice.GetChannelMask(DWORD@)
ms.date: 12/05/2018
ms.keywords: GetChannelMask, GetChannelMask method [XAudio2 Audio Mixing APIs], GetChannelMask method [XAudio2 Audio Mixing APIs],IXAudio2MasteringVoice interface, IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs],GetChannelMask method, IXAudio2MasteringVoice.GetChannelMask, IXAudio2MasteringVoice::GetChannelMask, xaudio2.ixaudio2masteringvoice_interface_getchannelmask, xaudio2/IXAudio2MasteringVoice::GetChannelMask
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2MasteringVoice::GetChannelMask
 - xaudio2/IXAudio2MasteringVoice::GetChannelMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2MasteringVoice.GetChannelMask
---

# IXAudio2MasteringVoice::GetChannelMask


## -description

Returns the channel mask for this voice.

## -parameters

### -param pChannelmask [out]

Returns the channel mask for this voice. This corresponds to the <b>dwChannelMask</b> member of the  <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a> structure.

## -returns

This method does not return a value.

## -remarks

The <i>pChannelMask</i> argument is a bit-mask of the various channels in the speaker geometry reported by the audio system. This information is needed for the <a href="/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize">X3DAudioInitialize</a> <i>SpeakerChannelMask</i> parameter.



The X3DAUDIO.H header declares a number of <b>SPEAKER_</b> positional defines to decode these channels masks.



Examples include:




```
SPEAKER_STEREO // SPEAKER_FRONT_LEFT (0x1) | SPEAKER_FRONT_RIGHT (0x2) 

SPEAKER_5POINT1 // SPEAKER_FRONT_LEFT (0x1) | SPEAKER_FRONT_RIGHT (0x2)
                                    // | SPEAKER_FRONT_CENTER (0x4)
                                    // | SPEAKER_LOW_FREQUENCY (0x8)
                                    // | SPEAKER_BACK_LEFT (0x10) | SPEAKER_BACK_RIGHT (0x20)
```


<div class="alert"><b>Note</b>  For the DirectX SDK versions of XAUDIO, the channel mask for the output device was obtained via the <b>IXAudio2::GetDeviceDetails</b> method, which doesn't exist in Windows 8 and later.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice">IXAudio2MasteringVoice</a>
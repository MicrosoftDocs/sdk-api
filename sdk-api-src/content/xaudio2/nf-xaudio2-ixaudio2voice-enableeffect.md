---
UID: NF:xaudio2.IXAudio2Voice.EnableEffect
title: IXAudio2Voice::EnableEffect (xaudio2.h)
description: Enables the effect at a given position in the effect chain of the voice.helpviewer_keywords: ["EnableEffect","EnableEffect method [XAudio2 Audio Mixing APIs]","EnableEffect method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","EnableEffect method","IXAudio2Voice.EnableEffect","IXAudio2Voice::EnableEffect","xaudio2.ixaudio2voice_interface_enableeffect","xaudio2/IXAudio2Voice::EnableEffect"]
old-location: xaudio2\ixaudio2voice_interface_enableeffect.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.EnableEffect(UINT32,UINT32)
ms.date: 12/05/2018
ms.keywords: EnableEffect, EnableEffect method [XAudio2 Audio Mixing APIs], EnableEffect method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],EnableEffect method, IXAudio2Voice.EnableEffect, IXAudio2Voice::EnableEffect, xaudio2.ixaudio2voice_interface_enableeffect, xaudio2/IXAudio2Voice::EnableEffect
f1_keywords:
- xaudio2/IXAudio2Voice.EnableEffect
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- XAudio2.h
api_name:
- IXAudio2Voice.EnableEffect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXAudio2Voice::EnableEffect


## -description


Enables the effect at a given position in the effect chain of the voice.


## -parameters




### -param EffectIndex [in]

Zero-based index of an effect in the effect chain of the voice.


### -param X2DEFAULT

TBD




#### - OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="https://docs.microsoft.com/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview for more information. 


## -returns



Returns S_OK if successful; otherwise, an error code. See <a href="https://docs.microsoft.com/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of error codes.






## -remarks



Be careful when you enable an effect while the voice that hosts it is running. Such an action can result in a problem if the effect significantly changes the audio's pitch or volume.



The effects in a given XAudio2 voice's effect chain must consume and produce audio at that voice's processing sample rate. The only aspect of the audio format they can change is the channel count. For example a reverb effect can convert mono data to 5.1. The client can use the <a href="https://docs.microsoft.com/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor">XAUDIO2_EFFECT_DESCRIPTOR</a> structure's <b>OutputChannels</b> field to specify the number of channels it wants each effect to produce. Each effect in an effect chain must produce a number of channels that the next effect can consume. Any calls to <b>IXAudio2Voice::EnableEffect</b> or <a href="https://docs.microsoft.com/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect">IXAudio2Voice::DisableEffect</a> that would make the effect chain stop fulfilling these requirements will fail.



<b>EnableEffect</b> takes effect immediately when you call it from an XAudio2 callback with an <i>OperationSet</i> of <b>XAUDIO2_COMMIT_NOW</b>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="https://docs.microsoft.com/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>
 

 


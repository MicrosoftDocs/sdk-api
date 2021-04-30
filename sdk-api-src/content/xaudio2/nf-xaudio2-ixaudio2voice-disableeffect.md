---
UID: NF:xaudio2.IXAudio2Voice.DisableEffect
title: IXAudio2Voice::DisableEffect (xaudio2.h)
description: Disables the effect at a given position in the effect chain of the voice.
helpviewer_keywords: ["DisableEffect","DisableEffect method [XAudio2 Audio Mixing APIs]","DisableEffect method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","DisableEffect method","IXAudio2Voice.DisableEffect","IXAudio2Voice::DisableEffect","xaudio2.ixaudio2voice_interface_disableeffect","xaudio2/IXAudio2Voice::DisableEffect"]
old-location: xaudio2\ixaudio2voice_interface_disableeffect.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.DisableEffect(UINT32,UINT32)
ms.date: 12/05/2018
ms.keywords: DisableEffect, DisableEffect method [XAudio2 Audio Mixing APIs], DisableEffect method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],DisableEffect method, IXAudio2Voice.DisableEffect, IXAudio2Voice::DisableEffect, xaudio2.ixaudio2voice_interface_disableeffect, xaudio2/IXAudio2Voice::DisableEffect
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
 - IXAudio2Voice::DisableEffect
 - xaudio2/IXAudio2Voice::DisableEffect
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
 - IXAudio2Voice.DisableEffect
---

# IXAudio2Voice::DisableEffect


## -description

Disables the effect at a given position in the effect chain of the voice.

## -parameters

### -param EffectIndex [in]

Zero-based index of an effect in the effect chain of the voice.

### -param X2DEFAULT

TBD

### -param OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview for more information.

## -returns

Returns S_OK if successful; otherwise, an error code. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of valid error codes.

## -remarks

The effects in a given XAudio2 voice's effect chain must consume and produce audio at that voice's processing sample rate. The only aspect of the audio format they can change is the channel count. For example a reverb effect can convert mono data to 5.1. The client can use the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor">XAUDIO2_EFFECT_DESCRIPTOR</a> structure's <b>OutputChannels</b> field to specify the number of channels it wants each effect to produce. Each effect in an effect chain must produce a number of channels that the next effect can consume. Any calls to <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect">IXAudio2Voice::EnableEffect</a> or <b>IXAudio2Voice::DisableEffect</b> that would make the effect chain stop fulfilling these requirements will fail.



Disabling an effect immediately removes it from the processing graph. Any pending audio in the effect—such as a reverb tail—is not played. Be careful disabling an effect while the voice that hosts it is running. This can result in an audible artifact if the effect significantly changes the audio's pitch or volume.



<b>DisableEffect</b> takes effect immediately when called from an XAudio2 callback with an <i>OperationSet</i> of <b>XAUDIO2_COMMIT_NOW</b>.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>
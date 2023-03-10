---
UID: NF:xaudio2.IXAudio2Voice.SetEffectChain
title: IXAudio2Voice::SetEffectChain (xaudio2.h)
description: Replaces the effect chain of the voice.
helpviewer_keywords: ["IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","SetEffectChain method","IXAudio2Voice.SetEffectChain","IXAudio2Voice::SetEffectChain","SetEffectChain","SetEffectChain method [XAudio2 Audio Mixing APIs]","SetEffectChain method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","xaudio2.ixaudio2voice_interface_seteffectchain","xaudio2/IXAudio2Voice::SetEffectChain"]
old-location: xaudio2\ixaudio2voice_interface_seteffectchain.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.SetEffectChain(const XAUDIO2_EFFECT_CHAIN)
ms.date: 12/05/2018
ms.keywords: IXAudio2Voice interface [XAudio2 Audio Mixing APIs],SetEffectChain method, IXAudio2Voice.SetEffectChain, IXAudio2Voice::SetEffectChain, SetEffectChain, SetEffectChain method [XAudio2 Audio Mixing APIs], SetEffectChain method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, xaudio2.ixaudio2voice_interface_seteffectchain, xaudio2/IXAudio2Voice::SetEffectChain
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
 - IXAudio2Voice::SetEffectChain
 - xaudio2/IXAudio2Voice::SetEffectChain
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
 - IXAudio2Voice.SetEffectChain
---

# IXAudio2Voice::SetEffectChain


## -description

Replaces the effect chain of the voice.

## -parameters

### -param pEffectChain [in, optional]

Pointer to an <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> structure that describes the new effect chain to use. If NULL is passed, the current effect chain is removed.

<div class="alert"><b>Note</b>  If <i>pEffectChain</i> is non-NULL, the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> structure that it points to must specify at least one effect.</div>
<div> </div>

## -returns

Returns S_OK if successful; otherwise, an error code. 



See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

The number of output channels allowed for a voice's effect chain is locked at creation of the voice. If you create the voice with an effect chain, any new effect chain passed to <b>SetEffectChain</b> must have the same number of input and output channels as the original effect chain. If you create the voice without an effect chain, the number of output channels allowed for the effect chain will default to the number of input channels for the voice. If any part of effect chain creation fails, none of it is applied.



After you attach an effect to an XAudio2 voice, XAudio2 takes control of the effect, and the client should not make any further calls to it. The simplest way to ensure this is to release all pointers to the effect.



It is invalid to call <b>SetEffectChain</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). If you call <b>SetEffectChain</b> within a callback, it returns XAUDIO2_E_INVALID_CALL.



The <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> that is passed in as the pEffectChain argument and any <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor">XAUDIO2_EFFECT_DESCRIPTOR</a> information contained within it are no longer needed after <b>SetEffectChain</b> successfully completes, and may be deleted immediately after <b>SetEffectChain</b> is called.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--create-an-effect-chain">How to: Create an Effect Chain</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>
---
UID: NF:xaudio2.IXAudio2Voice.SetEffectChain
title: IXAudio2Voice::SetEffectChain
author: windows-sdk-content
description: Replaces the effect chain of the voice.
old-location: xaudio2\ixaudio2voice_interface_seteffectchain.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.SetEffectChain(const XAUDIO2_EFFECT_CHAIN)
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IXAudio2Voice interface [XAudio2 Audio Mixing APIs],SetEffectChain method, IXAudio2Voice.SetEffectChain, IXAudio2Voice::SetEffectChain, SetEffectChain, SetEffectChain method [XAudio2 Audio Mixing APIs], SetEffectChain method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, xaudio2.ixaudio2voice_interface_seteffectchain, xaudio2/IXAudio2Voice::SetEffectChain
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - xaudio2.h
api_name:
 - IXAudio2Voice.SetEffectChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2Voice::SetEffectChain


## -description


Replaces the effect chain of the voice.


## -parameters




### -param pEffectChain [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/7519f0e0-e063-4849-ba58-675f42e91241">XAUDIO2_EFFECT_CHAIN</a> structure that describes the new effect chain to use. If NULL is passed, the current effect chain is removed.

<div class="alert"><b>Note</b>  If <i>pEffectChain</i> is non-NULL, the <a href="https://msdn.microsoft.com/7519f0e0-e063-4849-ba58-675f42e91241">XAUDIO2_EFFECT_CHAIN</a> structure that it points to must specify at least one effect.</div>
<div> </div>

## -returns



Returns S_OK if successful; otherwise, an error code. 



See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.




## -remarks



The number of output channels allowed for a voice's effect chain is locked at creation of the voice. If you create the voice with an effect chain, any new effect chain passed to <b>SetEffectChain</b> must have the same number of input and output channels as the original effect chain. If you create the voice without an effect chain, the number of output channels allowed for the effect chain will default to the number of input channels for the voice. If any part of effect chain creation fails, none of it is applied.



After you attach an effect to an XAudio2 voice, XAudio2 takes control of the effect, and the client should not make any further calls to it. The simplest way to ensure this is to release all pointers to the effect.



It is invalid to call <b>SetEffectChain</b> from within a callback (that is, <a href="https://msdn.microsoft.com/D71C117F-826F-41E9-98F4-C6024B3C5103">IXAudio2EngineCallback</a> or <a href="https://msdn.microsoft.com/FF78727D-16AE-40CB-BDE0-664687914FC0">IXAudio2VoiceCallback</a>). If you call <b>SetEffectChain</b> within a callback, it returns XAUDIO2_E_INVALID_CALL.



The <a href="https://msdn.microsoft.com/7519f0e0-e063-4849-ba58-675f42e91241">XAUDIO2_EFFECT_CHAIN</a> that is passed in as the pEffectChain argument and any <a href="https://msdn.microsoft.com/d2c7c640-9f6a-4fc0-bc87-35570281cec5">XAUDIO2_EFFECT_DESCRIPTOR</a> information contained within it are no longer needed after <b>SetEffectChain</b> successfully completes, and may be deleted immediately after <b>SetEffectChain</b> is called.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/4c33bd83-2654-cd6f-ea6c-bbc0d5872638">How to: Create an Effect Chain</a>



<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>
 

 


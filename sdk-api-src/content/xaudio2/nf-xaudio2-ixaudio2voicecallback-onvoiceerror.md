---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnVoiceError
title: IXAudio2VoiceCallback::OnVoiceError (xaudio2.h)
description: Called when a critical error occurs during voice processing.
helpviewer_keywords: ["IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs]","OnVoiceError method","IXAudio2VoiceCallback.OnVoiceError","IXAudio2VoiceCallback::OnVoiceError","OnVoiceError","OnVoiceError method [XAudio2 Audio Mixing APIs]","OnVoiceError method [XAudio2 Audio Mixing APIs]","IXAudio2VoiceCallback interface","xaudio2.ixaudio2voicecallback_interface_onvoiceerror","xaudio2/IXAudio2VoiceCallback::OnVoiceError"]
old-location: xaudio2\ixaudio2voicecallback_interface_onvoiceerror.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnVoiceError(void,HRESULT)
ms.date: 12/05/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnVoiceError method, IXAudio2VoiceCallback.OnVoiceError, IXAudio2VoiceCallback::OnVoiceError, OnVoiceError, OnVoiceError method [XAudio2 Audio Mixing APIs], OnVoiceError method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onvoiceerror, xaudio2/IXAudio2VoiceCallback::OnVoiceError
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
 - IXAudio2VoiceCallback::OnVoiceError
 - xaudio2/IXAudio2VoiceCallback::OnVoiceError
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
 - IXAudio2VoiceCallback.OnVoiceError
---

# IXAudio2VoiceCallback::OnVoiceError


## -description

Called when a critical error occurs during voice processing.

## -parameters

### -param pBufferContext

Context pointer that was assigned to the <b>pContext</b> member of the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure when the buffer was submitted.

### -param Error

The HRESULT code of the error encountered.

## -remarks

<b>OnVoiceError</b> is called in the event of an error during voice processing, such as a hardware XMA decoder error on the Xbox 360. The arguments report which buffer was being processed at the time of the error, and its HRESULT code. If the error is not recoverable by destroying and re-creating the voice, the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror">OnCriticalError</a> engine callback will be called as well. 


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--use-source-voice-callbacks">How to: Use Source Voice Callbacks</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>



<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>
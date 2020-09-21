---
UID: NF:xaudio2.IXAudio2Voice.SetOutputVoices
title: IXAudio2Voice::SetOutputVoices (xaudio2.h)
description: Designates a new set of submix or mastering voices to receive the output of the voice.
helpviewer_keywords: ["IXAudio2Voice interface [XAudio2 Audio Mixing APIs]","SetOutputVoices method","IXAudio2Voice.SetOutputVoices","IXAudio2Voice::SetOutputVoices","SetOutputVoices","SetOutputVoices method [XAudio2 Audio Mixing APIs]","SetOutputVoices method [XAudio2 Audio Mixing APIs]","IXAudio2Voice interface","xaudio2.ixaudio2voice_interface_setoutputvoices","xaudio2/IXAudio2Voice::SetOutputVoices"]
old-location: xaudio2\ixaudio2voice_interface_setoutputvoices.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.SetOutputVoices(const XAUDIO2_VOICE_SENDS)
ms.date: 12/05/2018
ms.keywords: IXAudio2Voice interface [XAudio2 Audio Mixing APIs],SetOutputVoices method, IXAudio2Voice.SetOutputVoices, IXAudio2Voice::SetOutputVoices, SetOutputVoices, SetOutputVoices method [XAudio2 Audio Mixing APIs], SetOutputVoices method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, xaudio2.ixaudio2voice_interface_setoutputvoices, xaudio2/IXAudio2Voice::SetOutputVoices
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
 - IXAudio2Voice::SetOutputVoices
 - xaudio2/IXAudio2Voice::SetOutputVoices
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
 - IXAudio2Voice.SetOutputVoices
---

# IXAudio2Voice::SetOutputVoices


## -description

Designates a new set of submix or mastering voices to receive the output of the voice.

## -parameters

### -param pSendList [in]

Array of <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends">XAUDIO2_VOICE_SENDS</a> structure pointers to destination voices. If <i>pSendList</i> is NULL, the voice will send its output to the current mastering voice. To set the voice to not send its output anywhere set the <b>OutputCount</b> member of <b>XAUDIO2_VOICE_SENDS</b> to 0. All of the voices in a send list must have the same input sample rate, see <a href="/windows/desktop/xaudio2/xaudio2-sample-rate-conversions">XAudio2 Sample Rate Conversions</a> for additional information.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

This method is only valid for source and submix voices. Mastering voices can not send audio to another voice.



After calling <b>SetOutputVoices</b> a voice's current send levels will be replaced by a default send matrix. The <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix">IXAudio2Voice::SetOutputMatrix</a> method must be called to set a custom matrix for the new sendlist.



It is invalid to call <b>SetOutputVoices</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). If <b>SetOutputVoices</b> is called within a callback, it returns XAUDIO2_E_INVALID_CALL.

<div class="alert"><b>Note</b>  Calling <b>SetOutputVoices</b> invalidates any send matrices previously set with <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix">IXAudio2Voice::SetOutputMatrix</a>.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>
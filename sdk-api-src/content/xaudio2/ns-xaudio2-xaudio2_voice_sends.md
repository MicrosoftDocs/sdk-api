---
UID: NS:xaudio2.XAUDIO2_VOICE_SENDS
title: XAUDIO2_VOICE_SENDS (xaudio2.h)
description: Defines a set of voices to receive data from a single output voice.
helpviewer_keywords: ["XAUDIO2_VOICE_SENDS","XAUDIO2_VOICE_SENDS structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_voice_sends","xaudio2/XAUDIO2_VOICE_SENDS"]
old-location: xaudio2\xaudio2_voice_sends.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_VOICE_SENDS
ms.date: 12/05/2018
ms.keywords: XAUDIO2_VOICE_SENDS, XAUDIO2_VOICE_SENDS structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_voice_sends, xaudio2/XAUDIO2_VOICE_SENDS
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
req.typenames: XAUDIO2_VOICE_SENDS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_VOICE_SENDS
 - xaudio2/XAUDIO2_VOICE_SENDS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_VOICE_SENDS
---

# XAUDIO2_VOICE_SENDS structure


## -description

Defines a set of voices to receive data from a single output voice.

## -struct-fields

### -field SendCount

Number of voices to receive the output of the voice. An <b>OutputCount</b> value of 0 indicates the voice should not send output to any voices.

### -field pSends

Array of <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor">XAUDIO2_SEND_DESCRIPTOR</a> structures describing destination voices and the filters that should be used when sending to the voices. This array should contain <b>SendCount</b> elements. If <b>SendCount</b> is 0 <b>pSends</b> should be NULL. Note that <b>pSends</b> cannot contain the same voice more than once.

## -remarks

If <b>pSends</b> is not NULL all of its elements must be non-NULL. To send output to the default mastering voice call <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices">IXAudio2Voice::SetOutputVoices</a> with the pSendList argument set to NULL.



Setting <b>SendCount</b> to 0 is useful for certain effects such as volume meters or file writers that don't generate any audio output to pass on to another voice.



If needed, a voice will perform a single sample rate conversion, from the voice's input sample rate to the input sample rate of the voice's output voices. Because only one sample rate conversion will be performed, all the voice's output voices must have the same input sample rate. If the input sample rates of the voice and its output voices are the same, no sample rate conversion is performed.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--change-voice-volume">How to: Change Voice Volume</a>



<a href="/windows/desktop/xaudio2/how-to--use-submix-voices">How to: Use Submix Voices</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice">IXAudio2::CreateSourceVoice</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice">IXAudio2::CreateSubmixVoice</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices">IXAudio2Voice::SetOutputVoices</a>



<a href="/windows/desktop/xaudio2/structures">XAudio Structures</a>



<a href="/windows/desktop/xaudio2/xaudio2-sample-rate-conversions">XAudio2 Sample Rate Conversions</a>
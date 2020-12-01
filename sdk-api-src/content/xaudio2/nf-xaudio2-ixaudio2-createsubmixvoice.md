---
UID: NF:xaudio2.IXAudio2.CreateSubmixVoice
title: IXAudio2::CreateSubmixVoice (xaudio2.h)
description: Creates and configures a submix voice.
helpviewer_keywords: ["CreateSubmixVoice","CreateSubmixVoice method [XAudio2 Audio Mixing APIs]","CreateSubmixVoice method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","IXAudio2 interface [XAudio2 Audio Mixing APIs]","CreateSubmixVoice method","IXAudio2.CreateSubmixVoice","IXAudio2::CreateSubmixVoice","xaudio2.ixaudio2_interface_createsubmixvoice","xaudio2/IXAudio2::CreateSubmixVoice"]
old-location: xaudio2\ixaudio2_interface_createsubmixvoice.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.CreateSubmixVoice(IXAudio2SubmixVoice@,UINT32,UINT32,UINT32,UINT32,const XAUDIO2_VOICE_SENDS,const XAUDIO2_EFFECT_CHAIN)
ms.date: 12/05/2018
ms.keywords: CreateSubmixVoice, CreateSubmixVoice method [XAudio2 Audio Mixing APIs], CreateSubmixVoice method [XAudio2 Audio Mixing APIs],IXAudio2 interface, IXAudio2 interface [XAudio2 Audio Mixing APIs],CreateSubmixVoice method, IXAudio2.CreateSubmixVoice, IXAudio2::CreateSubmixVoice, xaudio2.ixaudio2_interface_createsubmixvoice, xaudio2/IXAudio2::CreateSubmixVoice
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
 - IXAudio2::CreateSubmixVoice
 - xaudio2/IXAudio2::CreateSubmixVoice
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
 - IXAudio2.CreateSubmixVoice
---

# IXAudio2::CreateSubmixVoice


## -description

Creates and configures a submix voice.

## -parameters

### -param ppSubmixVoice [out]

On success, returns a pointer to the new <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice">IXAudio2SubmixVoice</a> object.

### -param InputChannels [in]

Number of channels in the input audio data of the submix voice. 
<i>InputChannels</i> must be less than or equal to XAUDIO2_MAX_AUDIO_CHANNELS.

### -param InputSampleRate [in]

Sample rate of the input audio data of submix voice. This rate must be a multiple of XAUDIO2_QUANTUM_DENOMINATOR. <i>InputSampleRate</i> must be between XAUDIO2_MIN_SAMPLE_RATE and XAUDIO2_MAX_SAMPLE_RATE.

### -param X2DEFAULT

TBD

### -param Flags [in]

Flags that specify the behavior of the submix voice. It can be 0 or the following:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XAUDIO2_VOICE_USEFILTER</td>
<td>The filter effect should be available on this voice.</td>
</tr>
</table>

### -param ProcessingStage [in]

An arbitrary number that specifies when this voice is processed with respect to other submix voices, if the XAudio2 engine is running other submix voices. The voice is processed after all other voices that include a smaller <i>ProcessingStage</i> value and before all other voices that include a larger <i>ProcessingStage</i> value. Voices that include the same <i>ProcessingStage</i> value are processed in any order. A submix voice cannot send to another submix voice with a lower or equal <i>ProcessingStage</i> value. This prevents audio being lost due to a submix cycle.

### -param pEffectChain [in, optional]

Pointer to a list of <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> structures that describe an effect chain to use in the submix voice.

### -param pSendList [in, optional]

Pointer to a list of <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends">XAUDIO2_VOICE_SENDS</a> structures that describe the set of destination voices for the submix voice. If <i>pSendList</i> is NULL, the send list will default to a single output to the first mastering voice created.

## -returns

Returns S_OK if successful; otherwise, an error code. 



See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

Submix voices receive the output of one or more source or submix voices. They process the output, and then send it to another submix voice or to a mastering voice.



A submix voice performs a sample rate conversion from the input sample rate to the input rate of its output voices in <i>pSendList</i>. If you specify multiple voice sends, they must all have the input same sample rate.



You cannot create any source or submix voices until a mastering voice exists, and you cannot destroy a mastering voice if any source or submix voices still exist.



When first created, submix voices are in the started state.



XAudio2 uses an internal memory pooler for voices with the same format. This means that memory allocation for voices will occur less frequently as more voices are created and then destroyed. To minimize just-in-time allocations, a title can create the anticipated maximum number of voices needed up front, and then delete them as necessary. Voices will then be reused from the XAudio2 pool. The memory pool is tied to an XAudio2 engine instance. You can reclaim all the memory used by an instance of the XAudio2 engine by destroying the XAudio2 object and recreating it as necessary (forcing the memory pool to grow via preallocation would have to be reapplied as needed).



It is invalid to call <b>CreateSubmixVoice</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). If you call <b>CreateSubmixVoice</b> within a callback, it returns XAUDIO2_E_INVALID_CALL.



The <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> that is passed in as the <i>pEffectChain</i> argument and any <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor">XAUDIO2_EFFECT_DESCRIPTOR</a> information contained within it are no longer needed after <b>CreateSubmixVoice</b> successfully completes, and may be deleted immediately after <b>CreateSubmixVoice</b> is called.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>



<a href="/windows/desktop/xaudio2/xaudio2-sample-rate-conversions">XAudio2 Sample Rate Conversions</a>
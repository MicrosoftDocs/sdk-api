---
UID: NF:xaudio2.IXAudio2.CreateSourceVoice
title: IXAudio2::CreateSourceVoice (xaudio2.h)
description: Creates and configures a source voice.
helpviewer_keywords: ["CreateSourceVoice","CreateSourceVoice method [XAudio2 Audio Mixing APIs]","CreateSourceVoice method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","IXAudio2 interface [XAudio2 Audio Mixing APIs]","CreateSourceVoice method","IXAudio2.CreateSourceVoice","IXAudio2::CreateSourceVoice","xaudio2.ixaudio2_interface_createsourcevoice","xaudio2/IXAudio2::CreateSourceVoice"]
old-location: xaudio2\ixaudio2_interface_createsourcevoice.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.CreateSourceVoice(IXAudio2SourceVoice@,const WAVEFORMATEX,UINT32,float,IXAudio2VoiceCallback,const XAUDIO2_VOICE_SENDS,const XAUDIO2_EFFECT_CHAIN)
ms.date: 12/05/2018
ms.keywords: CreateSourceVoice, CreateSourceVoice method [XAudio2 Audio Mixing APIs], CreateSourceVoice method [XAudio2 Audio Mixing APIs],IXAudio2 interface, IXAudio2 interface [XAudio2 Audio Mixing APIs],CreateSourceVoice method, IXAudio2.CreateSourceVoice, IXAudio2::CreateSourceVoice, xaudio2.ixaudio2_interface_createsourcevoice, xaudio2/IXAudio2::CreateSourceVoice
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
 - IXAudio2::CreateSourceVoice
 - xaudio2/IXAudio2::CreateSourceVoice
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
 - IXAudio2.CreateSourceVoice
---

# IXAudio2::CreateSourceVoice


## -description

Creates and configures a source voice.

## -parameters

### -param ppSourceVoice [out]

If successful, returns a pointer to the new <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a> object.

### -param pSourceFormat [in]

Pointer to a one of the structures in the table below. This structure contains the expected format for all audio buffers submitted to the source voice. 
XAudio2 supports PCM and ADPCM voice types. 

<table>
<tr>
<th>Format tag</th>
<th>Wave format structure</th>
<th>Size (in bytes)</th>
</tr>
<tr>
<td>WAVE_FORMAT_PCM (0x0001) </td>
<td>
<a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a>
</td>
<td>16</td>
</tr>
<tr>
<td>-or-</td>
<td>
<a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a>
</td>
<td>18</td>
</tr>
<tr>
<td>WAVE_FORMAT_IEEE_FLOAT (0x0003) [32-bit]</td>
<td>
<a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a>
</td>
<td>18</td>
</tr>
<tr>
<td>WAVE_FORMAT_ADPCM (0x0002) [MS-ADPCM]</td>
<td>
<a href="/previous-versions/dd743663(v=vs.85)">ADPCMWAVEFORMAT</a>
</td>
<td>50</td>
</tr>
<tr>
<td>WAVE_FORMAT_EXTENSIBLE (0xFFFE)</td>
<td>
<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a>
</td>
<td>40</td>
</tr>
</table>
 

XAudio2 supports the following PCM formats.


<ul>
<li>8-bit (unsigned) integer PCM

</li>
<li>16-bit integer PCM (optimal format for XAudio2)

</li>
<li>20-bit integer PCM (either in 24 or 32 bit containers)

</li>
<li>24-bit integer PCM (either in 24 or 32 bit containers)

</li>
<li>32-bit integer PCM

</li>
<li>32-bit float PCM (preferred format after 16-bit integer)
</li>
</ul>
The number of channels in a source voice must be less than or equal to XAUDIO2_MAX_AUDIO_CHANNELS. The sample rate of a source voice must be between XAUDIO2_MIN_SAMPLE_RATE and XAUDIO2_MAX_SAMPLE_RATE.

<div class="alert"><b>Note</b>  PCM data formats such as <a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a> and  <b>ADPCMWAVEFORMAT</b> that require more information than provided by <b>WAVEFORMATEX</b> have a <b>WAVEFORMATEX</b> structure as the first member in their format structures. When you create a source voice with one of those formats, cast the format's structure as a <b>WAVEFORMATEX</b> structure and use it as the value for <i>pSourceFormat</i>.</div>
<div> </div>

### -param X2DEFAULT

TBD

### -param Flags [in]

Flags that specify the behavior of the source voice. A flag can be 0 or a combination of one or more of the following:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XAUDIO2_VOICE_NOPITCH</td>
<td>No pitch control is available on the voice. </td>
</tr>
<tr>
<td>XAUDIO2_VOICE_NOSRC</td>
<td>No sample rate conversion is available on the voice. 
         The voice's outputs must have the same sample rate.<div class="alert"><b>Note</b>  The XAUDIO2_VOICE_NOSRC flag causes the voice to behave as though the XAUDIO2_VOICE_NOPITCH flag also is specified.</div>
<div> </div>
</td>
</tr>
<tr>
<td>XAUDIO2_VOICE_USEFILTER</td>
<td>The filter effect should be available on this voice. </td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The XAUDIO2_VOICE_MUSIC flag is not supported on Windows.</div>
<div> </div>

### -param MaxFrequencyRatio [in]

Highest allowable frequency ratio that can be set on this voice. The value for this argument must be between XAUDIO2_MIN_FREQ_RATIO and XAUDIO2_MAX_FREQ_RATIO. Subsequent calls to <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio">IXAudio2SourceVoice::SetFrequencyRatio</a> are clamped between XAUDIO2_MIN_FREQ_RATIO and <b>MaxFrequencyRatio</b>. 
The maximum value for this argument is defined as XAUDIO2_MAX_FREQ_RATIO, which allows pitch to be raised by up to 10 octaves.



If <i>MaxFrequencyRatio</i> is less than 1.0, the voice will use that ratio immediately after being created (rather than the default of 1.0).




<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>For XMA voices, there is one more restriction on the <i>MaxFrequencyRatio</i> argument and the voice's sample rate. The product of these two numbers cannot exceed XAUDIO2_MAX_RATIO_TIMES_RATE_XMA_MONO for one-channel voices or XAUDIO2_MAX_RATIO_TIMES_RATE_XMA_MULTICHANNEL for voices with any other number of channels. If the value specified for <i>MaxFrequencyRatio</i> is too high for the specified format, the call to <b>CreateSourceVoice</b> fails and produces a debug message.
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  You can use the lowest possible <i>MaxFrequencyRatio</i> value to reduce XAudio2's memory usage.</div>
<div> </div>

### -param pCallback [in, optional]

Pointer to a client-provided callback interface, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>.

### -param pEffectChain [in, optional]

Pointer to a list of <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> structures that describe an effect chain to use in the source voice.

### -param pSendList [in, out]

Pointer to a list of <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends">XAUDIO2_VOICE_SENDS</a> structures that describe the set of destination voices for the source voice. If pSendList is NULL, the send list defaults to a single output to the first mastering voice created.

## -returns

Returns S_OK if successful; otherwise, an error code. 



See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2-specific error codes.

## -remarks

Source voices read audio data from the client. They process the data and send it to the XAudio2 processing graph.



A source voice includes a variable-rate sample rate conversion, to convert data from the source format sample rate to the output rate required for the voice send list. If you use a NULL send list, the target sample rate will be the mastering voice's input sample rate. If you provide a single voice in pSendList, that voice's input sample rate is the target rate. If you provide multiple voices in the pSendList, all the source voice's output voices must be running at the same input sample rate.



You cannot create any source or submix voices until a mastering voice exists, and you cannot destroy a mastering voice if any source or submix voices still exist.



Source voices are always processed before any submix or mastering voices. This means that you do not need a ProcessingStage parameter to control the processing order.



When first created, source voices are in the stopped state.



XAudio2 uses an internal memory pooler for voices with the same format. This means memory allocation for voices will occur less frequently as more voices are created and then destroyed. To minimize just-in-time allocations, a title can create the anticipated maximum number of voices needed up front, and then delete them as necessary. Voices will then be reused from the XAudio2 pool. The memory pool is tied to an XAudio2 engine instance. You can reclaim all the memory used by an instance of the XAudio2 engine by destroying the XAudio2 object and recreating it as necessary (forcing the memory pool to grow via preallocation would have to be reapplied as needed).



It is invalid to call <b>CreateSourceVoice</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). If you call <b>CreateSourceVoice</b> within a callback, it returns XAUDIO2_E_INVALID_CALL.



The <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> that is passed in as the pEffectChain argument and any <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor">XAUDIO2_EFFECT_DESCRIPTOR</a> information contained within it are no longer needed after <b>CreateSourceVoice</b> successfully completes, and may be deleted immediately after <b>CreateSourceVoice</b> is called.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--build-a-basic-audio-processing-graph">How to: Build a Basic Audio Processing Graph</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>



<a href="/windows/desktop/xaudio2/xaudio2-sample-rate-conversions">XAudio2 Sample Rate Conversions</a>
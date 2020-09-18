---
UID: NS:xaudio2.XAUDIO2_BUFFER
title: XAUDIO2_BUFFER (xaudio2.h)
description: Represents an audio data buffer, used with IXAudio2SourceVoice::SubmitSourceBuffer.
helpviewer_keywords: ["XAUDIO2_BUFFER","XAUDIO2_BUFFER structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_buffer","xaudio2/XAUDIO2_BUFFER"]
old-location: xaudio2\xaudio2_buffer.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_BUFFER
ms.date: 12/05/2018
ms.keywords: XAUDIO2_BUFFER, XAUDIO2_BUFFER structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_buffer, xaudio2/XAUDIO2_BUFFER
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
req.typenames: XAUDIO2_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_BUFFER
 - xaudio2/XAUDIO2_BUFFER
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
 - XAUDIO2_BUFFER
---

# XAUDIO2_BUFFER structure


## -description

Represents an audio data buffer, used with <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer">IXAudio2SourceVoice::SubmitSourceBuffer</a>.

## -struct-fields

### -field Flags

Flags that provide additional information about the audio buffer. May be 0, or the following value.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XAUDIO2_END_OF_STREAM</td>
<td>Indicates that there cannot be any buffers in the queue
          after this buffer. The only effect of this flag is to suppress debug output warnings caused
          by starvation of the buffer queue. </td>
</tr>
</table>

### -field AudioBytes

Size of the audio data, in bytes. Must be no larger than XAUDIO2_MAX_BUFFER_BYTES (defined in xaudio2.h) for PCM data and no larger than XMA_READBUFFER_MAX_BYTES (defined in xma2defs.h) for XMA data.

<div class="alert"><b>Note</b>  XMA buffers submitted to an XAudio2 voice using <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer">IXAudio2SourceVoice::SubmitSourceBuffer</a> must contain complete XMA blocks. A complete XMA block must be equal in size to the <b>XMA2WAVEFORMATEX.BytesPerBlock</b> value, except for the last XMA block in a file, which may be shorter but will still be considered complete.</div>
<div> </div>

### -field pAudioData

Pointer to the audio data.

<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>
The memory allocated for a buffer containing XMA data must have a block alignment of 2048. This is accomplished using
         <b>XPhysicalAlloc</b> with the <i>ulAlignment</i> argument set to 2048.

</td>
</tr>
</table>

### -field PlayBegin

First sample in the buffer that should be played. 


For XMA buffers this value must be a multiple of 128 samples.

### -field PlayLength

Length of the region to be played, in samples. A value of zero means to play the entire buffer, and, in this case, <i>PlayBegin</i> must be zero as well. 
For ADPCM data this value must be a multiple of <b>wSamplesPerBlock</b> in the <b>ADPCMWAVEFORMAT</b> structure that contains this <b>XAUDIO2_BUFFER</b> structure.

### -field LoopBegin

First sample of the region to be looped. The value of <i>LoopBegin</i> must be less than <i>PlayBegin</i> + <i>PlayLength</i>. <i>LoopBegin</i> can be less than <i>PlayBegin</i>. <i>LoopBegin</i> must be 0 if <i>LoopCount</i> is 0.

### -field LoopLength

Length of the loop region, in samples. The value of <i>LoopBegin</i>+<i>LoopLength</i> must be greater than <i>PlayBegin</i> and less than <i>PlayBegin</i> + <i>PlayLength</i>. <i>LoopLength</i> must be zero if LoopCount is 0. If <i>LoopCount</i> is not 0 then a loop length of zero indicates the entire sample should be looped. 
For ADPCM data this value must be a multiple of <b>wSamplesPerBlock</b> in the <b>ADPCMWAVEFORMAT</b> structure that contains this <b>XAUDIO2_BUFFER</b> structure.

### -field LoopCount

Number of times to loop through the loop region. This value can be between 0 and XAUDIO2_MAX_LOOP_COUNT. If <i>LoopCount</i> is zero no looping is performed and <i>LoopBegin</i> and <i>LoopLength</i> must be 0. To loop forever, set <i>LoopCount</i> to XAUDIO2_LOOP_INFINITE.

### -field pContext

Context value to be passed back in callbacks to the client. This may be NULL.

## -remarks

XAudio2 audio data is interleaved, data from each channel is adjacent for a particular sample number. For example if there was a 4 channel wave playing into an XAudio2 source voice, the audio data would be a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, etc.



The <b>AudioBytes</b> and <b>pAudioData</b> members of <b>XAUDIO2_BUFFER</b> correspond to the size in bytes and contents of the 'data' RIFF chunk of the file being played. The contents of the chunk may need to be byte swapped when loading the file on Xbox 360.



Memory allocated to hold a <b>XAUDIO2_BUFFER</b> or <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma">XAUDIO2_BUFFER_WMA</a> structure can be freed as soon as the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer">IXAudio2SourceVoice::SubmitSourceBuffer</a> call it is passed to returns. The data the structure points to (<b>pAudioData</b> and <b>pDecodedPacketCumulativeBytes</b>, respectively) can't be freed until the buffer completes (as signaled by the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend">IXAudio2VoiceCallback::OnBufferEnd</a> callback) or the voice is stopped or destroyed.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--build-a-basic-audio-processing-graph">How to: Build a Basic Audio Processing Graph</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer">IXAudio2SourceVoice::SubmitSourceBuffer</a>



<a href="/windows/desktop/xaudio2/structures">XAudio2 Structures</a>
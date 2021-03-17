---
UID: NF:xaudio2.IXAudio2SourceVoice.SubmitSourceBuffer
title: IXAudio2SourceVoice::SubmitSourceBuffer (xaudio2.h)
description: Adds a new audio buffer to the voice queue.
helpviewer_keywords: ["IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","SubmitSourceBuffer method","IXAudio2SourceVoice.SubmitSourceBuffer","IXAudio2SourceVoice::SubmitSourceBuffer","SubmitSourceBuffer","SubmitSourceBuffer method [XAudio2 Audio Mixing APIs]","SubmitSourceBuffer method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","xaudio2.ixaudio2sourcevoice_interface_submitsourcebuffer","xaudio2/IXAudio2SourceVoice::SubmitSourceBuffer"]
old-location: xaudio2\ixaudio2sourcevoice_interface_submitsourcebuffer.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.SubmitSourceBuffer(const XAUDIO2_BUFFER,const XAUDIO2_BUFFER_WMA)
ms.date: 12/05/2018
ms.keywords: IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],SubmitSourceBuffer method, IXAudio2SourceVoice.SubmitSourceBuffer, IXAudio2SourceVoice::SubmitSourceBuffer, SubmitSourceBuffer, SubmitSourceBuffer method [XAudio2 Audio Mixing APIs], SubmitSourceBuffer method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, xaudio2.ixaudio2sourcevoice_interface_submitsourcebuffer, xaudio2/IXAudio2SourceVoice::SubmitSourceBuffer
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
 - IXAudio2SourceVoice::SubmitSourceBuffer
 - xaudio2/IXAudio2SourceVoice::SubmitSourceBuffer
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
 - IXAudio2SourceVoice.SubmitSourceBuffer
---

# IXAudio2SourceVoice::SubmitSourceBuffer


## -description

Adds a new audio buffer to the voice queue.

## -parameters

### -param pBuffer [in]

Pointer to an <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure to queue.

### -param X2DEFAULT

TBD

### -param pBufferWMA [in]

Pointer to an additional <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma">XAUDIO2_BUFFER_WMA</a> structure used when submitting WMA data.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

The voice processes and plays back the buffers in its queue in the order that they were submitted.



The <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure includes details about the audio buffer's location and size, the part of the buffer that should actually be played, the loop region (if any) and loop count, the context pointer to be used in any callbacks relating to this buffer, and an optional XAUDIO2_END_OF_STREAM flag that indicates that it is the last buffer of a contiguous sound.



If the voice is started and has no buffers queued, the new buffer will start playing immediately. If the voice is stopped, the buffer is added to the voice's queue and will be played when the voice starts.



If only part of the given buffer should be played, the <b>PlayBegin</b> and <b>PlayLength</b> fields in the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> can be used to specify the region to be played. A <b>PlayLength</b> value of 0 means to play the entire buffer (and in this case <b>PlayBegin</b> must be 0 as well).



If all or part of the buffer should be played in a continuous loop, the <b>LoopBegin</b>, <b>LoopLength</b> and <b>LoopCount</b> fields in <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> can be used to specify the characteristics of the loop region. A <b>LoopBegin</b> value of XAUDIO2_NO_LOOP_REGION means that no looping should be performed, and in this case <b>LoopLength</b> and <b>LoopCount</b> must be given as 0. If a loop region is specified, it must be non-empty (<b>LoopLength</b> &gt; 0), and the loop count must be between 1 and XAUDIO2_MAX_LOOP_COUNT inclusive (or XAUDIO2_LOOP_INFINITE to specify an endless loop which will only end when <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop">IXAudio2SourceVoice::ExitLoop</a> is called). A loop count of <i>N</i> means to skip backwards N times, i.e. to play the loop region <i>N</i>+1 times.



If an explicit play region is specified, it must begin and end within the given audio buffer (or, in the compressed case, within the set of samples that the buffer will decode to). In addition, the loop region cannot end past the end of the play region.



<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>For certain audio formats, there may be additional restrictions on the valid endpoints of any play or loop regions; e.g. for XMA buffers, the regions can only begin or end at 128-sample boundaries in the decoded audio.
</td>
</tr>
</table>
 

The <i>pBuffer</i> pointer can be reused or freed immediately after calling this method, but the actual audio data referenced by <i>pBuffer</i> must remain valid until the buffer has been fully consumed by XAudio2 (which is indicated by the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend">IXAudio2VoiceCallback::OnBufferEnd</a> callback).



Up to XAUDIO2_MAX_QUEUED_BUFFERS buffers can be queued on a voice at any one time.



<b>SubmitSourceBuffer</b> takes effect immediately when called from an XAudio2 callback with an OperationSet of XAUDIO2_COMMIT_NOW.


<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>This method can be called from an Xbox system thread (most other XAudio2 methods cannot). However, a maximum of two source buffers can be submitted from a system thread at a time.</td>
</tr>
</table>
 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--build-a-basic-audio-processing-graph">How to: Build a Basic Audio Processing Graph</a>



<a href="/windows/desktop/xaudio2/how-to--stream-a-sound-from-disk">How to: Stream a Sound from Disk</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>
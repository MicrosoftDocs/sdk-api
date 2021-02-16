---
UID: NF:xaudio2.IXAudio2SourceVoice.Stop
title: IXAudio2SourceVoice::Stop (xaudio2.h)
description: Stops consumption of audio by the current voice.
helpviewer_keywords: ["IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","Stop method","IXAudio2SourceVoice.Stop","IXAudio2SourceVoice::Stop","Stop","Stop method [XAudio2 Audio Mixing APIs]","Stop method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","xaudio2.ixaudio2sourcevoice_interface_stop","xaudio2/IXAudio2SourceVoice::Stop"]
old-location: xaudio2\ixaudio2sourcevoice_interface_stop.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.Stop(UINT32,UINT32)
ms.date: 12/05/2018
ms.keywords: IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],Stop method, IXAudio2SourceVoice.Stop, IXAudio2SourceVoice::Stop, Stop, Stop method [XAudio2 Audio Mixing APIs], Stop method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, xaudio2.ixaudio2sourcevoice_interface_stop, xaudio2/IXAudio2SourceVoice::Stop
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
 - IXAudio2SourceVoice::Stop
 - xaudio2/IXAudio2SourceVoice::Stop
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
 - IXAudio2SourceVoice.Stop
---

# IXAudio2SourceVoice::Stop


## -description

Stops consumption of audio by the current voice.

## -parameters

### -param X2DEFAULT

TBD

### -param Flags [in]

Flags that control how the voice is stopped. Can be 0 or the following: 


<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XAUDIO2_PLAY_TAILS</td>
<td>Continue emitting effect output after the voice is stopped. </td>
</tr>
</table>

### -param OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview for more information.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

All source buffers that are queued on the voice and the current cursor position are preserved. This allows the voice to continue from where it left off, when it is restarted. The <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-flushsourcebuffers">IXAudio2SourceVoice::FlushSourceBuffers</a> method can be used to flush queued source buffers.



By default, any pending output from voice effects—for example, reverb tails—is not played. Instead, the voice is immediately rendered silent. The XAUDIO2_PLAY_TAILS flag can be used to continue emitting effect output after the voice stops running.



A voice stopped with the XAUDIO2_PLAY_TAILS flag stops consuming source buffers, but continues to process its effects and send audio to its destination voices. A voice in this state can later be stopped completely by calling <b>Stop</b> again with the Flags argument set to 0. This enables stopping a voice with XAUDIO2_PLAY_TAILS, waiting sufficient time for any audio being produced by its effects to finish, and then fully stopping the voice by calling <b>Stop</b> again without XAUDIO2_PLAY_TAILS. This technique allows voices with effects to be stopped gracefully while ensuring idle voices will not continue to be processed after they have finished producing audio.



<b>Stop</b> is always asynchronous, even if called within a callback.



<div class="alert"><b>Note</b>  XAudio2 never calls any voice callbacks for a voice if the voice is stopped (even if it was stopped with XAUDIO2_PLAY_TAILS).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>
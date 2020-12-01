---
UID: NS:xaudio2.XAUDIO2_BUFFER_WMA
title: XAUDIO2_BUFFER_WMA (xaudio2.h)
description: Used with IXAudio2SourceVoice::SubmitSourceBuffer when submitting xWMA data.
helpviewer_keywords: ["XAUDIO2_BUFFER_WMA","XAUDIO2_BUFFER_WMA structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_buffer_wma","xaudio2/XAUDIO2_BUFFER_WMA"]
old-location: xaudio2\xaudio2_buffer_wma.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_BUFFER_WMA
ms.date: 12/05/2018
ms.keywords: XAUDIO2_BUFFER_WMA, XAUDIO2_BUFFER_WMA structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_buffer_wma, xaudio2/XAUDIO2_BUFFER_WMA
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
req.typenames: XAUDIO2_BUFFER_WMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_BUFFER_WMA
 - xaudio2/XAUDIO2_BUFFER_WMA
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
 - XAUDIO2_BUFFER_WMA
---

# XAUDIO2_BUFFER_WMA structure


## -description

Used with <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer">IXAudio2SourceVoice::SubmitSourceBuffer</a> when submitting xWMA data.

## -struct-fields

### -field pDecodedPacketCumulativeBytes

Decoded packet cumulative data size array, each element is the number of bytes accumulated after the corresponding xWMA packet is decoded in order, must have <b>PacketCount</b> elements.

### -field PacketCount

Number of xWMA packets submitted, must be &gt;= 1 and divide evenly into the respective <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a>.<b>AudioBytes</b> value passed to <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer">IXAudio2SourceVoice::SubmitSourceBuffer</a>.

## -remarks

When streaming an xWMA file a few packets at a time, XAUDIO2_END_OF_STREAM should be specified on the last packet. Alternatively, the application may call <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-discontinuity">IXAudio2SourceVoice::Discontinuity</a> after submitting the last packet.



In addition, when streaming an xWMA file a few packets at a time, the application should subtract <b>pDecodedPacketCumulativeBytes</b>[<b>PacketCount</b>-1] of the previous packet from all the entries of the currently submitted packet.



The members of <b>XAUDIO2_BUFFER_WMA</b> correspond to values contained in the 'dpds' RIFF chunk of the xWMA file being played. <b>PacketCount</b> will correspond to the size in UINT32s of the chunk. <b>pDecodedPacketCumulativeBytes</b> will correspond to a UINT32 buffer containing the contents of the chunk. The contents of the buffer will need to be byte swapped when loading the buffer on Xbox 360.



Memory allocated to hold a <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> or <b>XAUDIO2_BUFFER_WMA</b> structure can be freed as soon as the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer">IXAudio2SourceVoice::SubmitSourceBuffer</a> call it is passed to returns. The data the structure points to (<b>pAudioData</b> and <b>pDecodedPacketCumulativeBytes</b>, respectively) can't be freed until the buffer completes (as signaled by the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend">IXAudio2VoiceCallback::OnBufferEnd</a> callback) or the voice is stopped and destroyed.



XAUDIO 2.8 in Windows 8.x does not support xWMA decoding. Use Windows Media Foundation APIs to perform the decoding from WMA to PCM instead. This functionality is available in the DirectX SDK versions of XAUDIO and in XAUDIO 2.9 in Windows 10.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>
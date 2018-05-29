---
UID: NS:xaudio2.XAUDIO2_BUFFER_WMA
title: XAUDIO2_BUFFER_WMA
author: windows-sdk-content
description: Used with IXAudio2SourceVoice::SubmitSourceBuffer when submitting xWMA data.
old-location: xaudio2\xaudio2_buffer_wma.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_BUFFER_WMA
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: XAUDIO2_BUFFER_WMA, XAUDIO2_BUFFER_WMA structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_buffer_wma, xaudio2/XAUDIO2_BUFFER_WMA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: XAUDIO2_BUFFER_WMA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	xaudio2.h
api_name:
-	XAUDIO2_BUFFER_WMA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAUDIO2_BUFFER_WMA structure


## -description


Used with <a href="https://msdn.microsoft.com/D4A1FB27-12F6-41A0-9ACF-3F13EBB27165">IXAudio2SourceVoice::SubmitSourceBuffer</a> when submitting xWMA data.


## -struct-fields




### -field pDecodedPacketCumulativeBytes

Decoded packet cumulative data size array, each element is the number of bytes accumulated after the corresponding xWMA packet is decoded in order, must have <b>PacketCount</b> elements.


### -field PacketCount

Number of xWMA packets submitted, must be &gt;= 1 and divide evenly into the respective <a href="https://msdn.microsoft.com/b6c2a08b-6abb-4e6a-8acb-6f8983aef95f">XAUDIO2_BUFFER</a>.<b>AudioBytes</b> value passed to <a href="https://msdn.microsoft.com/D4A1FB27-12F6-41A0-9ACF-3F13EBB27165">IXAudio2SourceVoice::SubmitSourceBuffer</a>.


## -remarks



When streaming an xWMA file a few packets at a time, XAUDIO2_END_OF_STREAM should be specified on the last packet. Alternatively, the application may call <a href="https://msdn.microsoft.com/457F95F5-1A93-4918-8EC1-43851D25CB31">IXAudio2SourceVoice::Discontinuity</a> after submitting the last packet.



In addition, when streaming an xWMA file a few packets at a time, the application should subtract <b>pDecodedPacketCumulativeBytes</b>[<b>PacketCount</b>-1] of the previous packet from all the entries of the currently submitted packet.



The members of <b>XAUDIO2_BUFFER_WMA</b> correspond to values contained in the 'dpds' RIFF chunk of the xWMA file being played. <b>PacketCount</b> will correspond to the size in UINT32s of the chunk. <b>pDecodedPacketCumulativeBytes</b> will correspond to a UINT32 buffer containing the contents of the chunk. The contents of the buffer will need to be byte swapped when loading the buffer on Xbox 360.



Memory allocated to hold a <a href="https://msdn.microsoft.com/b6c2a08b-6abb-4e6a-8acb-6f8983aef95f">XAUDIO2_BUFFER</a> or <b>XAUDIO2_BUFFER_WMA</b> structure can be freed as soon as the <a href="https://msdn.microsoft.com/D4A1FB27-12F6-41A0-9ACF-3F13EBB27165">IXAudio2SourceVoice::SubmitSourceBuffer</a> call it is passed to returns. The data the structure points to (<b>pAudioData</b> and <b>pDecodedPacketCumulativeBytes</b>, respectively) can't be freed until the buffer completes (as signaled by the <a href="https://msdn.microsoft.com/803D1DB9-8C10-4821-BB0F-DDF85B11B9B3">IXAudio2VoiceCallback::OnBufferEnd</a> callback) or the voice is stopped and destroyed.



XAUDIO 2.8 in Windows 8.x does not support xWMA decoding. Use Windows Media Foundation APIs to perform the decoding from WMA to PCM instead. This functionality is available in the DirectX SDK versions of XAUDIO and in XAUDIO 2.9 in Windows 10.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 


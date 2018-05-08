---
UID: NN:xaudio2.IXAudio2SourceVoice
title: IXAudio2SourceVoice
author: windows-driver-content
description: Use a source voice to submit audio data to the XAudio2 processing pipeline.
old-location: xaudio2\ixaudio2sourcevoice.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IXAudio2SourceVoice, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs], IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2sourcevoice, xaudio2/IXAudio2SourceVoice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xaudio2.lib
-	xaudio2.dll
api_name:
-	IXAudio2SourceVoice
product: Windows
targetos: Windows
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2SourceVoice interface


## -description


Use a source voice to submit audio data to the XAudio2 processing pipeline.You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXAudio2SourceVoice</b> interface inherits from <a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>. <b>IXAudio2SourceVoice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXAudio2SourceVoice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/457F95F5-1A93-4918-8EC1-43851D25CB31">Discontinuity </a>
</td>
<td align="left" width="63%">
Notifies an XAudio2 voice that no more buffers are coming after the last one that is currently in its queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4C65F991-2796-4D06-A02A-91708D805731">ExitLoop</a>
</td>
<td align="left" width="63%">
Stops looping the voice when it reaches the end of the current loop region. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/623DADA3-2E61-4997-8DFC-EFEC2716FCDE">FlushSourceBuffers</a>
</td>
<td align="left" width="63%">
Removes all pending audio buffers from the voice queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A87D428-9C2D-4B89-B817-360C13F60145">GetFrequencyRatio</a>
</td>
<td align="left" width="63%">
Returns the frequency adjustment ratio of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6F466C04-D5AD-4B66-A806-9B379582D4DF">GetState</a>
</td>
<td align="left" width="63%">
Returns the voice's current cursor position data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58D458C3-528B-4696-8A24-2D66B93695C3">SetFrequencyRatio</a>
</td>
<td align="left" width="63%">
Sets the frequency adjustment ratio of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27413C97-12C6-4BCF-9F78-36116C84EECC">SetSourceSampleRate</a>
</td>
<td align="left" width="63%">
Reconfigures the voice to consume source data at a different sample rate than the rate specified when the voice was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts consumption and processing of audio by the voice. Delivers the result to any connected submix or mastering voices, or to the output device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops consumption of audio by the current voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D4A1FB27-12F6-41A0-9ACF-3F13EBB27165">SubmitSourceBuffer</a>
</td>
<td align="left" width="63%">
Adds a new audio buffer to the voice queue.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/93408116-1c1f-307f-7e1f-090f2663ff0b">How to: Change Voice Pitch</a>



<a href="https://msdn.microsoft.com/48b80a66-91c1-973f-069b-6f63422d7154">How to: Stream a Sound from Disk</a>



<a href="https://msdn.microsoft.com/0bace0c5-9171-efd8-9a38-2c2b3452f73f">How to: Use Source Voice Callbacks</a>



<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>



<a href="https://msdn.microsoft.com/96691e00-9ed0-b31c-fbe9-4daaba0daf98">XAudio2 Interfaces</a>
 

 


---
UID: NN:xaudio2.IXAudio2VoiceCallback
title: IXAudio2VoiceCallback
author: windows-driver-content
description: The IXAudio2VoiceCallback interface contains methods that notify the client when certain events happen in a given IXAudio2SourceVoice.
old-location: xaudio2\ixaudio2voicecallback.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IXAudio2VoiceCallback, IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs], IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs], described, xaudio2.ixaudio2voicecallback, xaudio2/IXAudio2VoiceCallback
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
-	IXAudio2VoiceCallback
product: Windows
targetos: Windows
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2VoiceCallback interface


## -description


The <b>IXAudio2VoiceCallback</b> interface contains methods that notify the client when certain events happen in a given <a href="https://msdn.microsoft.com/116DD0E0-8F0B-4934-A48D-FDBE0D0DF049">IXAudio2SourceVoice</a>. 

This interface should be implemented by the XAudio2 client. XAudio2 calls these methods through an interface pointer provided by the client in the <a href="https://msdn.microsoft.com/5F37327B-A749-4D2D-A664-7DC45A13FF9A">IXAudio2::CreateSourceVoice</a> method. Methods in this interface return void, rather than an HRESULT. 


See the <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> topic for restrictions on callback implementation.
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>IXAudio2VoiceCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/803D1DB9-8C10-4821-BB0F-DDF85B11B9B3">OnBufferEnd</a>
</td>
<td align="left" width="63%">
Called when the voice finishes processing a buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2A21636B-0142-4FCF-8F86-F07A33EBD20C">OnBufferStart</a>
</td>
<td align="left" width="63%">
Called when the voice is about to start processing a new audio buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4D768113-14D6-448C-A035-47F3B83D7425">OnLoopEnd</a>
</td>
<td align="left" width="63%">
Called when the voice reaches the end position of a loop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/852FBAA1-F390-441F-96DE-5086FB644B44">OnStreamEnd</a>
</td>
<td align="left" width="63%">
Called when the voice has just finished playing a contiguous audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A4468567-9497-49EB-94A9-6A76FFFFB470">OnVoiceError</a>
</td>
<td align="left" width="63%">
Called when a critical error occurs during voice processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6285B11C-AFE5-4FF6-91E1-A77593F445C1">OnVoiceProcessingPassEnd</a>
</td>
<td align="left" width="63%">
Called just after the processing pass for the voice ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4C5AAC1D-22D9-44D4-A7DD-65772369182F">OnVoiceProcessingPassStart</a>
</td>
<td align="left" width="63%">
Called during each processing pass for each voice, just before XAudio2 reads data from the voice's buffer queue.

</td>
</tr>
</table> 


## -members

The <b>IXAudio2VoiceCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/803D1DB9-8C10-4821-BB0F-DDF85B11B9B3">OnBufferEnd</a>
</td>
<td align="left" width="63%">
Called when the voice finishes processing a buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2A21636B-0142-4FCF-8F86-F07A33EBD20C">OnBufferStart</a>
</td>
<td align="left" width="63%">
Called when the voice is about to start processing a new audio buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4D768113-14D6-448C-A035-47F3B83D7425">OnLoopEnd</a>
</td>
<td align="left" width="63%">
Called when the voice reaches the end position of a loop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/852FBAA1-F390-441F-96DE-5086FB644B44">OnStreamEnd</a>
</td>
<td align="left" width="63%">
Called when the voice has just finished playing a contiguous audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A4468567-9497-49EB-94A9-6A76FFFFB470">OnVoiceError</a>
</td>
<td align="left" width="63%">
Called when a critical error occurs during voice processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6285B11C-AFE5-4FF6-91E1-A77593F445C1">OnVoiceProcessingPassEnd</a>
</td>
<td align="left" width="63%">
Called just after the processing pass for the voice ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4C5AAC1D-22D9-44D4-A7DD-65772369182F">OnVoiceProcessingPassStart</a>
</td>
<td align="left" width="63%">
Called during each processing pass for each voice, just before XAudio2 reads data from the voice's buffer queue.

</td>
</tr>
</table>Called when the voice finishes processing a buffer. 

Called when the voice is about to start processing a new audio buffer.

Called when the voice reaches the end position of a loop.

Called when the voice has just finished playing a contiguous audio stream.

Called when a critical error occurs during voice processing.

Called just after the processing pass for the voice ends.

Called during each processing pass for each voice, just before XAudio2 reads data from the voice's buffer queue.

 

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/48b80a66-91c1-973f-069b-6f63422d7154">How to: Stream a Sound from Disk</a>



<a href="https://msdn.microsoft.com/0bace0c5-9171-efd8-9a38-2c2b3452f73f">How to: Use Source Voice Callbacks</a>



<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>



<a href="https://msdn.microsoft.com/96691e00-9ed0-b31c-fbe9-4daaba0daf98">XAudio2 Interfaces</a>
 

 


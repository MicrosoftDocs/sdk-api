---
UID: NN:xaudio2.IXAudio2VoiceCallback
title: IXAudio2VoiceCallback
author: windows-sdk-content
description: The IXAudio2VoiceCallback interface contains methods that notify the client when certain events happen in a given IXAudio2SourceVoice.
old-location: xaudio2\ixaudio2voicecallback.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXAudio2VoiceCallback, IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs], IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2voicecallback, xaudio2/IXAudio2VoiceCallback
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - IXAudio2VoiceCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2VoiceCallback interface


## -description


The <b>IXAudio2VoiceCallback</b> interface contains methods that notify the client when certain events happen in a given <a href="https://msdn.microsoft.com/en-us/library/Ee415914(v=VS.85).aspx">IXAudio2SourceVoice</a>. 

This interface should be implemented by the XAudio2 client. XAudio2 calls these methods through an interface pointer provided by the client in the <a href="https://msdn.microsoft.com/en-us/library/Ee418607(v=VS.85).aspx">IXAudio2::CreateSourceVoice</a> method. Methods in this interface return void, rather than an HRESULT. 


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
<a href="https://msdn.microsoft.com/en-us/library/Ee418474(v=VS.85).aspx">OnBufferEnd</a>
</td>
<td align="left" width="63%">
Called when the voice finishes processing a buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418475(v=VS.85).aspx">OnBufferStart</a>
</td>
<td align="left" width="63%">
Called when the voice is about to start processing a new audio buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418476(v=VS.85).aspx">OnLoopEnd</a>
</td>
<td align="left" width="63%">
Called when the voice reaches the end position of a loop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418477(v=VS.85).aspx">OnStreamEnd</a>
</td>
<td align="left" width="63%">
Called when the voice has just finished playing a contiguous audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418478(v=VS.85).aspx">OnVoiceError</a>
</td>
<td align="left" width="63%">
Called when a critical error occurs during voice processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418479(v=VS.85).aspx">OnVoiceProcessingPassEnd</a>
</td>
<td align="left" width="63%">
Called just after the processing pass for the voice ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418480(v=VS.85).aspx">OnVoiceProcessingPassStart</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Ee418474(v=VS.85).aspx">OnBufferEnd</a>
</td>
<td align="left" width="63%">
Called when the voice finishes processing a buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418475(v=VS.85).aspx">OnBufferStart</a>
</td>
<td align="left" width="63%">
Called when the voice is about to start processing a new audio buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418476(v=VS.85).aspx">OnLoopEnd</a>
</td>
<td align="left" width="63%">
Called when the voice reaches the end position of a loop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418477(v=VS.85).aspx">OnStreamEnd</a>
</td>
<td align="left" width="63%">
Called when the voice has just finished playing a contiguous audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418478(v=VS.85).aspx">OnVoiceError</a>
</td>
<td align="left" width="63%">
Called when a critical error occurs during voice processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418479(v=VS.85).aspx">OnVoiceProcessingPassEnd</a>
</td>
<td align="left" width="63%">
Called just after the processing pass for the voice ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418480(v=VS.85).aspx">OnVoiceProcessingPassStart</a>
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
 

 


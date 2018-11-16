---
UID: NN:austream.IAudioMediaStream
title: IAudioMediaStream
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\iaudiomediastream.htm
tech.root: DirectShow
ms.assetid: b4098876-6c11-4cc6-8b6d-16edc02316f3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAudioMediaStream, IAudioMediaStream interface [DirectShow], IAudioMediaStream interface [DirectShow],described, IAudioMediaStreamInterface, austream/IAudioMediaStream, dshow.iaudiomediastream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: austream.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IAudioMediaStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAudioMediaStream</code> interface controls audio media streams by providing methods that set and get the stream's format. This interface inherits from the <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a> interface and is used to create one or more <a href="https://msdn.microsoft.com/53deec43-30ca-472e-9a82-750049686d2a">IAudioStreamSample</a> objects. You can also use it to set and retrieve the stream data's current format.

This interface is currently defined only for PCM format audio data.

For sample code that implements the audio streaming interfaces, see <a href="https://msdn.microsoft.com/3fe2996b-b4de-40ad-bd02-d850a45f3a2c">Multimedia Streaming Sample Code</a>.

Like video, audio is contained in a self-describing container object. Implement this interface when an object needs to control streaming audio.

Use this interface when you want to generate audio in your application.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioMediaStream</b> interface inherits from <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a>. <b>IAudioMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7d62a2c-54a9-4690-8ba0-34e927f9f093">CreateSample</a>
</td>
<td align="left" width="63%">
Creates an audio stream sample for use with this stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df582b90-f537-42cf-a83e-109a20446d8a">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the stream data's current format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5925f373-c862-4215-9877-5bb4d5411d36">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the format for the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a>
 

 


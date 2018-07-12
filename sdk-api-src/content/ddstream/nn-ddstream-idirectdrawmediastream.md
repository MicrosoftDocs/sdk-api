---
UID: NN:ddstream.IDirectDrawMediaStream
title: IDirectDrawMediaStream
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\idirectdrawmediastream.htm
old-project: DirectShow
ms.assetid: 858af0c3-9e22-45d8-ab08-307eb39a8977
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IDirectDrawMediaStream, IDirectDrawMediaStream interface [DirectShow], IDirectDrawMediaStream interface [DirectShow],described, IDirectDrawMediaStreamInterface, ddstream/IDirectDrawMediaStream, dshow.idirectdrawmediastream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ddstream.h
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
tech.root: 
req.typenames: VIDEOMEMORYINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddstream.h
api_name:
 - IDirectDrawMediaStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectDrawMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IDirectDrawMediaStream</code> interface controls media streams that appear on Microsoft DirectDraw surfaces. To stream to a DirectDraw surface, DirectDraw must support the video stream format.

For sample code that implements the multimedia streaming interfaces, see <a href="https://msdn.microsoft.com/3fe2996b-b4de-40ad-bd02-d850a45f3a2c">Multimedia Streaming Sample Code</a>.

This interface isn't intended for implementation by application developers. It is exposed on DirectDraw media streams that can be added to a DirectShow multimedia stream.

Use this interface when you want to send a video stream to a DirectDraw surface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawMediaStream</b> interface inherits from <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a>. <b>IDirectDrawMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85041c71-f9fc-48fc-8fe2-fec21efb831b">CreateSample</a>
</td>
<td align="left" width="63%">
Creates a stream sample using the specified DirectDraw surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44c505fe-70d9-49bd-9135-8a6dc2c72e98">GetDirectDraw</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the DirectDraw object used by the current media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3729bbe6-3504-46b3-9978-e66afc56344f">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current media stream's format and, optionally, its desired format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24133185-0d5f-41fc-b381-ef982db46dd1">GetTimePerFrame</a>
</td>
<td align="left" width="63%">
Retrieves the average frames per second from a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffa425c5-5f81-4963-bf23-2139d8b245b3">SetDirectDraw</a>
</td>
<td align="left" width="63%">
Sets the current media stream's DirectDraw object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/465b4f0c-40e1-4aec-be62-0b55c29fa05e">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the current media stream's format. If the stream already has allocated samples and the sample format doesn't match the specified format, this method fails.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a>
 

 


---
UID: NN:mmstream.IMediaStream
title: IMediaStream
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\imediastream.htm
old-project: DirectShow
ms.assetid: 97f5dfdc-5941-4b58-a618-1c7e9f6665e1
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMediaStream, IMediaStream interface [DirectShow], IMediaStream interface [DirectShow],described, IMediaStreamInterface, dshow.imediastream, mmstream/IMediaStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmstream.h
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
req.typenames: STREAM_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMediaStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <b>IMediaStream</b> interface provides access to the characteristics of a media stream, such as the stream's media type and purpose ID. It also has methods that create data samples.

For sample code that implements the multimedia streaming interfaces, see <a href="https://msdn.microsoft.com/3fe2996b-b4de-40ad-bd02-d850a45f3a2c">Multimedia Streaming Sample Code</a>.

Implement this interface when you want to add media type-specific functionality to your media stream. This interface is implemented on multimedia stream objects. <b>IMediaStream</b> provides generic sample-creation methods, but you usually want to write a more powerful version of these methods that will take advantage of your media type's specific characteristics.

Use this interface when your application needs to access a stream's media type information and create data samples.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a035797d-ebf2-40c2-b1a3-b903a691b7d2">AllocateSample</a>
</td>
<td align="left" width="63%">
Allocates a new stream sample object for the current media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acefa476-e607-45b4-854d-840e948af029">CreateSharedSample</a>
</td>
<td align="left" width="63%">
Creates a new stream sample that shares the same backing object as the existing sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4ecae45-e2bf-44dd-8901-0892c02d708c">GetInformation</a>
</td>
<td align="left" width="63%">
Retrieves the stream's purpose ID and media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09af4bfc-2427-4992-b508-fe9a7ac150d7">GetMultiMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the multimedia stream that contains the specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa774875-1cf2-4792-a492-fef64571ae8f">SendEndOfStream</a>
</td>
<td align="left" width="63%">
Forces the current stream to end. If the current stream isn't writable, this method does nothing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a228547-7187-4a7a-8850-2681e0ccb13e">SetSameFormat</a>
</td>
<td align="left" width="63%">
Sets the media stream to the same format as a previous stream.

</td>
</tr>
</table> 


---
UID: NN:mmstream.IMediaStream
title: IMediaStream (mmstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\imediastream.htm
tech.root: DirectShow
ms.assetid: 97f5dfdc-5941-4b58-a618-1c7e9f6665e1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaStream, IMediaStream interface [DirectShow], IMediaStream interface [DirectShow],described, IMediaStreamInterface, dshow.imediastream, mmstream/IMediaStream
ms.topic: interface
f1_keywords: ["mmstream/IMediaStream"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <b>IMediaStream</b> interface provides access to the characteristics of a media stream, such as the stream's media type and purpose ID. It also has methods that create data samples.

For sample code that implements the multimedia streaming interfaces, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/multimedia-streaming-sample-code">Multimedia Streaming Sample Code</a>.

Implement this interface when you want to add media type-specific functionality to your media stream. This interface is implemented on multimedia stream objects. <b>IMediaStream</b> provides generic sample-creation methods, but you usually want to write a more powerful version of these methods that will take advantage of your media type's specific characteristics.

Use this interface when your application needs to access a stream's media type information and create data samples.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaStream</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample">AllocateSample</a>
</td>
<td align="left" width="63%">
Allocates a new stream sample object for the current media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample">CreateSharedSample</a>
</td>
<td align="left" width="63%">
Creates a new stream sample that shares the same backing object as the existing sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imediastream-getinformation">GetInformation</a>
</td>
<td align="left" width="63%">
Retrieves the stream's purpose ID and media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imediastream-getmultimediastream">GetMultiMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the multimedia stream that contains the specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imediastream-sendendofstream">SendEndOfStream</a>
</td>
<td align="left" width="63%">
Forces the current stream to end. If the current stream isn't writable, this method does nothing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imediastream-setsameformat">SetSameFormat</a>
</td>
<td align="left" width="63%">
Sets the media stream to the same format as a previous stream.

</td>
</tr>
</table> 


---
UID: NN:ddstream.IDirectDrawMediaStream
title: IDirectDrawMediaStream (ddstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IDirectDrawMediaStream","IDirectDrawMediaStream interface [DirectShow]","IDirectDrawMediaStream interface [DirectShow]","described","IDirectDrawMediaStreamInterface","ddstream/IDirectDrawMediaStream","dshow.idirectdrawmediastream"]
old-location: dshow\idirectdrawmediastream.htm
tech.root: DirectShow
ms.assetid: 858af0c3-9e22-45d8-ab08-307eb39a8977
ms.date: 12/05/2018
ms.keywords: IDirectDrawMediaStream, IDirectDrawMediaStream interface [DirectShow], IDirectDrawMediaStream interface [DirectShow],described, IDirectDrawMediaStreamInterface, ddstream/IDirectDrawMediaStream, dshow.idirectdrawmediastream
f1_keywords:
- ddstream/IDirectDrawMediaStream
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ddstream.h
api_name:
- IDirectDrawMediaStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IDirectDrawMediaStream</code> interface controls media streams that appear on Microsoft DirectDraw surfaces. To stream to a DirectDraw surface, DirectDraw must support the video stream format.

For sample code that implements the multimedia streaming interfaces, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/multimedia-streaming-sample-code">Multimedia Streaming Sample Code</a>.

This interface isn't intended for implementation by application developers. It is exposed on DirectDraw media streams that can be added to a DirectShow multimedia stream.

Use this interface when you want to send a video stream to a DirectDraw surface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawMediaStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>. <b>IDirectDrawMediaStream</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample">CreateSample</a>
</td>
<td align="left" width="63%">
Creates a stream sample using the specified DirectDraw surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-getdirectdraw">GetDirectDraw</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the DirectDraw object used by the current media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-getformat">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current media stream's format and, optionally, its desired format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-gettimeperframe">GetTimePerFrame</a>
</td>
<td align="left" width="63%">
Retrieves the average frames per second from a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-setdirectdraw">SetDirectDraw</a>
</td>
<td align="left" width="63%">
Sets the current media stream's DirectDraw object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-setformat">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the current media stream's format. If the stream already has allocated samples and the sample format doesn't match the specified format, this method fails.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>
 

 


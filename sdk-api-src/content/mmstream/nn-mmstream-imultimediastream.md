---
UID: NN:mmstream.IMultiMediaStream
title: IMultiMediaStream (mmstream.h)
description: Note  This interface is deprecated.
old-location: dshow\imultimediastream.htm
tech.root: DirectShow
ms.assetid: 8be6c74f-9290-48b4-ad66-8d7d7cc94174
ms.date: 12/05/2018
ms.keywords: IMultiMediaStream, IMultiMediaStream interface [DirectShow], IMultiMediaStream interface [DirectShow],described, IMultiMediaStreamInterface, dshow.imultimediastream, mmstream/IMultiMediaStream
f1_keywords:
- mmstream/IMultiMediaStream
dev_langs:
- c++
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
- IMultiMediaStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMultiMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IMultiMediaStream</code> interface is exposed by the AMMultimediaStream object. It contains methods for enumerating the media streams, retrieving information about them, and running and stopping them.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultiMediaStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMultiMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMultiMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams">EnumMediaStreams</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of the multimedia stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getendofstreameventhandle">GetEndOfStreamEventHandle</a>
</td>
<td align="left" width="63%">
Retrieves an event that is signaled when the multimedia stream completes playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getinformation">GetInformation</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the multimedia stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream">GetMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by purpose ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getstate">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the multimedia stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-gettime">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the current stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-seek">Seek</a>
</td>
<td align="left" width="63%">
Seeks all of the media streams to a new position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate">SetState</a>
</td>
<td align="left" width="63%">
Runs or stops the multimedia stream object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>
 

 


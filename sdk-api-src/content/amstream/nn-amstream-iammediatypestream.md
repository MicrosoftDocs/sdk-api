---
UID: NN:amstream.IAMMediaTypeStream
title: IAMMediaTypeStream (amstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAMMediaTypeStream","IAMMediaTypeStream interface [DirectShow]","IAMMediaTypeStream interface [DirectShow]","described","IAMMediaTypeStreamInterface","amstream/IAMMediaTypeStream","dshow.iammediatypestream"]
old-location: dshow\iammediatypestream.htm
tech.root: dshow
ms.assetid: 6ca1bad2-625b-4415-8311-acd5443452c1
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeStream, IAMMediaTypeStream interface [DirectShow], IAMMediaTypeStream interface [DirectShow],described, IAMMediaTypeStreamInterface, amstream/IAMMediaTypeStream, dshow.iammediatypestream
f1_keywords:
- amstream/IAMMediaTypeStream
dev_langs:
- c++
req.header: amstream.h
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
- amstream.h
api_name:
- IAMMediaTypeStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMediaTypeStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
This interface contains methods for creating multimedia streams with arbitrary media types. Use this interface if you need to create a multimedia stream with a format that is not supported by the other Microsoft DirectShow multimedia streaming interfaces.

<div class="alert"><b>Note</b>  For video streams, use the <a href="https://docs.microsoft.com/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream</a> interface instead of this interface. For audio streams, use the <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream</a> interface.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaTypeStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>. <b>IAMMediaTypeStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMMediaTypeStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammediatypestream-createsample">CreateSample</a>
</td>
<td align="left" width="63%">
Creates a stream sample and optionally specifies the sample buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammediatypestream-getformat">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the format of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammediatypestream-getstreamallocatorrequirements">GetStreamAllocatorRequirements</a>
</td>
<td align="left" width="63%">
Retrieves the allocator requirements for the stream. This method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammediatypestream-setformat">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the format of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammediatypestream-setstreamallocatorrequirements">SetStreamAllocatorRequirements</a>
</td>
<td align="left" width="63%">
Sets the allocator requirements for the stream. This method is not currently implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>
 

 


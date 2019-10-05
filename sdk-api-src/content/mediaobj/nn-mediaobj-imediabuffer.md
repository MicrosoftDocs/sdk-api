---
UID: NN:mediaobj.IMediaBuffer
title: IMediaBuffer (mediaobj.h)
author: windows-sdk-content
description: The IMediaBuffer interface provides methods for manipulating a data buffer. Buffers passed to the IMediaObject::ProcessInput and ProcessOutput methods must implement this interface.
old-location: dshow\imediabuffer.htm
tech.root: DirectShow
ms.assetid: 74d72ca6-f899-43fc-bdea-5208d920f314
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaBuffer, IMediaBuffer interface [DirectShow], IMediaBuffer interface [DirectShow],described, IMediaBufferInterface, dshow.imediabuffer, mediaobj/IMediaBuffer
ms.topic: interface
f1_keywords: 
 - "mediaobj/IMediaBuffer"
dev_langs:
 - c++
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaBuffer interface


## -description



The <code>IMediaBuffer</code> interface provides methods for manipulating a data buffer. Buffers passed to the <b>IMediaObject::ProcessInput</b> and <b>ProcessOutput</b> methods must implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength">GetBufferAndLength</a>
</td>
<td align="left" width="63%">
Retrieves the buffer and the size of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getmaxlength">GetMaxLength</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of bytes this buffer can hold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-setlength">SetLength</a>
</td>
<td align="left" width="63%">
Specifies the length of the data currently in the buffer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/implementing-imediabuffer">Implementing IMediaBuffer</a>
 

 


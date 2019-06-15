---
UID: NN:objidl.ISequentialStream
title: ISequentialStream (objidl.h)
author: windows-sdk-content
description: The ISequentialStream interface supports simplified sequential access to stream objects. The IStream interface inherits its Read and Write methods from ISequentialStream.
old-location: stg\isequentialstream.htm
tech.root: Stg
ms.assetid: c1d33800-d2f1-4942-92fa-e115f524c23c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISequentialStream, ISequentialStream interface [Structured Storage], ISequentialStream interface [Structured Storage],described, _stg_isequentialstream, objidl/ISequentialStream, stg.isequentialstream
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ISequentialStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISequentialStream interface


## -description


The 
<b>ISequentialStream</b> interface supports simplified sequential access to stream objects. The 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface inherits its 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">Write</a> methods from 
<b>ISequentialStream</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISequentialStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISequentialStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISequentialStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>
</td>
<td align="left" width="63%">
Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">Write</a>
</td>
<td align="left" width="63%">
Writes a specified number of bytes to the stream object starting at the current seek pointer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>
 

 


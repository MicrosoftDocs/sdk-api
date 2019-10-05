---
UID: NN:d2d1_1.ID2D1GdiMetafile
title: ID2D1GdiMetafile (d2d1_1.h)
author: windows-sdk-content
description: A Direct2D resource that wraps a WMF, EMF, or EMF+ metafile.
old-location: direct2d\id2d1gdimetafile.htm
tech.root: Direct2D
ms.assetid: 36A454EC-7DE0-4610-B49C-7FBBD21C425C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1GdiMetafile, ID2D1GdiMetafile interface [Direct2D], ID2D1GdiMetafile interface [Direct2D],described, d2d1_1/ID2D1GdiMetafile, direct2d.id2d1gdimetafile
ms.topic: interface
f1_keywords: 
 - "d2d1_1/ID2D1GdiMetafile"
dev_langs:
 - c++
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GdiMetafile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1GdiMetafile interface


## -description


A Direct2D resource that wraps a WMF, EMF, or EMF+ metafile.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GdiMetafile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1GdiMetafile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GdiMetafile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds">GetBounds</a>
</td>
<td align="left" width="63%">
 Gets the bounds of the metafile, in DIPs, as reported in the metafile’s header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-stream">Stream</a>
</td>
<td align="left" width="63%">
This method streams the contents of the command  to the given metafile  sink. 

</td>
</tr>
</table> 


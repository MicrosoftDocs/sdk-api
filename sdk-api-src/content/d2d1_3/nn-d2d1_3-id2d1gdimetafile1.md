---
UID: NN:d2d1_3.ID2D1GdiMetafile1
title: ID2D1GdiMetafile1 (d2d1_3.h)
description: This interface performs all the same functions as the existing ID2D1GdiMetafile interface. It also enables accessing the metafile DPI and bounds.helpviewer_keywords: ["ID2D1GdiMetafile1","ID2D1GdiMetafile1 interface [Direct2D]","ID2D1GdiMetafile1 interface [Direct2D]","described","d2d1_3/ID2D1GdiMetafile1","direct2d.id2d1gdimetafile1"]
old-location: direct2d\id2d1gdimetafile1.htm
tech.root: Direct2D
ms.assetid: 7a05abd6-ea75-8496-85c3-efa1e307482d
ms.date: 12/05/2018
ms.keywords: ID2D1GdiMetafile1, ID2D1GdiMetafile1 interface [Direct2D], ID2D1GdiMetafile1 interface [Direct2D],described, d2d1_3/ID2D1GdiMetafile1, direct2d.id2d1gdimetafile1
f1_keywords:
- d2d1_3/ID2D1GdiMetafile1
dev_langs:
- c++
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
- ID2D1GdiMetafile1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1GdiMetafile1 interface


## -description


This interface performs all the same functions as the existing ID2D1GdiMetafile interface. It also enables accessing the metafile DPI and bounds.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GdiMetafile1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a>. <b>ID2D1GdiMetafile1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GdiMetafile1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1gdimetafile1-getdpi">GetDpi</a>
</td>
<td align="left" width="63%">
Gets the DPI reported by the metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1gdimetafile1-getsourcebounds">GetSourceBounds</a>
</td>
<td align="left" width="63%">
Gets the bounds of the metafile in source space in DIPs. This corresponds      
    to the frame rect in an EMF/EMF+.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a>
 

 


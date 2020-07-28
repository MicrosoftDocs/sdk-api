---
UID: NN:d2d1effectauthor.ID2D1SourceTransform
title: ID2D1SourceTransform (d2d1effectauthor.h)
description: Represents a CPU-based rasterization stage in the transform pipeline graph.
helpviewer_keywords: ["ID2D1SourceTransform","ID2D1SourceTransform interface [Direct2D]","ID2D1SourceTransform interface [Direct2D]","described","d2d1effectauthor/ID2D1SourceTransform","direct2d.id2d1sourcetransform"]
old-location: direct2d\id2d1sourcetransform.htm
tech.root: Direct2D
ms.assetid: A2B3E8E1-8F7F-4AFA-B1CE-5E8A5FCD9B70
ms.date: 12/05/2018
ms.keywords: ID2D1SourceTransform, ID2D1SourceTransform interface [Direct2D], ID2D1SourceTransform interface [Direct2D],described, d2d1effectauthor/ID2D1SourceTransform, direct2d.id2d1sourcetransform
f1_keywords:
- d2d1effectauthor/ID2D1SourceTransform
dev_langs:
- c++
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d2d1.lib
- d2d1.dll
api_name:
- ID2D1SourceTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SourceTransform interface


## -description


Represents a CPU-based rasterization stage in the transform  pipeline graph.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SourceTransform</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform">ID2D1Transform</a>. <b>ID2D1SourceTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SourceTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1sourcetransform-draw">Draw</a>
</td>
<td align="left" width="63%">
Draws the transform to the GPU–based Direct2D pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1sourcetransform-setrenderinfo">SetRenderInfo</a>
</td>
<td align="left" width="63%">
Sets the render information for the transform.

</td>
</tr>
</table> 


## -remarks



<b>ID2D1SourceTransform</b> specializes an implementation of the Shantzis calculations to a transform implemented as the source of an effect graph with the data being provided from sytem memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform">ID2D1Transform</a>
 

 


---
UID: NN:d2d1effectauthor.ID2D1Transform
title: ID2D1Transform (d2d1effectauthor.h)
description: Represents the base interface for all of the transforms implemented by the transform author.
old-location: direct2d\id2d1transform.htm
tech.root: Direct2D
ms.assetid: 8A0CD795-A6D8-4817-9676-58C11DDAAEBD
ms.date: 12/05/2018
ms.keywords: ID2D1Transform, ID2D1Transform interface [Direct2D], ID2D1Transform interface [Direct2D],described, d2d1effectauthor/ID2D1Transform, direct2d.id2d1transform
f1_keywords:
- d2d1effectauthor/ID2D1Transform
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
- ID2D1Transform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Transform interface


## -description


Represents the base interface for all of the transforms implemented by the transform author.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Transform</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>. <b>ID2D1Transform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Transform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect">MapInputRectsToOutputRect</a>
</td>
<td align="left" width="63%">
Performs the inverse mapping to <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects">MapOutputRectToInputRects</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect">MapInvalidRect</a>
</td>
<td align="left" width="63%">
Sets the input rectangles for this rendering pass into the transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects">MapOutputRectToInputRects</a>
</td>
<td align="left" width="63%">
Allows a transform to state how it would map a rectangle requested on its output to a set of sample rectangles on its input.

</td>
</tr>
</table> 


## -remarks



Transforms are aggregated by effect authors. This interface  provides a common interface for implementing the Shantzis rectangle calculations which is the basis for all the transform processing in Direct2D imaging extensions.  These  calculations are described in the paper <a href="https://dl.acm.org/citation.cfm?id=192191">A model for efficient and flexible image computing</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>
 

 


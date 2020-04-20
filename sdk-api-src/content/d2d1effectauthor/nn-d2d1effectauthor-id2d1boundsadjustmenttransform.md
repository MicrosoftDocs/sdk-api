---
UID: NN:d2d1effectauthor.ID2D1BoundsAdjustmentTransform
title: ID2D1BoundsAdjustmentTransform (d2d1effectauthor.h)
description: A support transform for effects to modify the output rectangle of the previous effect or bitmap.helpviewer_keywords: ["ID2D1BoundsAdjustmentTransform","ID2D1BoundsAdjustmentTransform interface [Direct2D]","ID2D1BoundsAdjustmentTransform interface [Direct2D]","described","d2d1effectauthor/ID2D1BoundsAdjustmentTransform","direct2d.id2d1boundadjustmenttransform"]
old-location: direct2d\id2d1boundadjustmenttransform.htm
tech.root: Direct2D
ms.assetid: 40482670-2989-47B2-9558-FF017C8A2FBB
ms.date: 12/05/2018
ms.keywords: ID2D1BoundsAdjustmentTransform, ID2D1BoundsAdjustmentTransform interface [Direct2D], ID2D1BoundsAdjustmentTransform interface [Direct2D],described, d2d1effectauthor/ID2D1BoundsAdjustmentTransform, direct2d.id2d1boundadjustmenttransform
f1_keywords:
- d2d1effectauthor/ID2D1BoundsAdjustmentTransform
dev_langs:
- c++
req.header: d2d1effectauthor.h
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
- d2d1effectauthor.h
api_name:
- ID2D1BoundsAdjustmentTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1BoundsAdjustmentTransform interface


## -description


A support transform for effects to modify the output rectangle of the previous effect or bitmap.  




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1BoundsAdjustmentTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1BoundsAdjustmentTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1BoundsAdjustmentTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1boundsadjustmenttransform-getoutputbounds">GetOutputBounds</a>
</td>
<td align="left" width="63%">
Returns the output rectangle of the support transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1boundsadjustmenttransform-setoutputbounds">SetOutputBounds</a>
</td>
<td align="left" width="63%">
This sets the output bounds for the support transform.

</td>
</tr>
</table> 


## -remarks



The support transform can be used for two different reasons.

<ul>
<li>
To indicate that a region of its input image is already transparent black.  The expanded area will be treated as transparent black.

This can increase efficiency for rendering bitmaps.

</li>
<li>
To increase the size of the input image.

</li>
</ul>



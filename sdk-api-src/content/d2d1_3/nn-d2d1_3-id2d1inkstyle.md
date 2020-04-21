---
UID: NN:d2d1_3.ID2D1InkStyle
title: ID2D1InkStyle (d2d1_3.h)
description: Represents a collection of style properties to be used by methods like ID2D1DeviceContext2::DrawInkwhen rendering ink. The ink style defines the nib (pen tip) shape and transform.helpviewer_keywords: ["ID2D1InkStyle","ID2D1InkStyle interface [Direct2D]","ID2D1InkStyle interface [Direct2D]","described","d2d1_3/ID2D1InkStyle","direct2d.id2d1inkstyle"]
old-location: direct2d\id2d1inkstyle.htm
tech.root: Direct2D
ms.assetid: 03853FA5-1377-42FB-A4C2-50069DDF6E2D
ms.date: 12/05/2018
ms.keywords: ID2D1InkStyle, ID2D1InkStyle interface [Direct2D], ID2D1InkStyle interface [Direct2D],described, d2d1_3/ID2D1InkStyle, direct2d.id2d1inkstyle
f1_keywords:
- d2d1_3/ID2D1InkStyle
dev_langs:
- c++
req.header: d2d1_3.h
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d2d1_3.dll
api_name:
- ID2D1InkStyle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1InkStyle interface


## -description


Represents a collection of style properties to be used by methods like <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink">ID2D1DeviceContext2::DrawInk</a>when rendering ink. The ink style defines the nib (pen tip) shape and transform.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1InkStyle</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1InkStyle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1InkStyle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1inkstyle-getnibshape">GetNibShape</a>
</td>
<td align="left" width="63%">
Retrieves the pre-transform nib shape for this style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1inkstyle-getnibtransform">GetNibTransform</a>
</td>
<td align="left" width="63%">
Retrieves the transform to be applied to this style's nib shape.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1inkstyle-setnibshape">SetNibShape</a>
</td>
<td align="left" width="63%">
Sets the pre-transform nib shape for this style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-setnibtransform">SetNibTransform</a>
</td>
<td align="left" width="63%">Overloaded. Sets the transform to apply to this style's nib shape.

</td>
</tr>
</table> 


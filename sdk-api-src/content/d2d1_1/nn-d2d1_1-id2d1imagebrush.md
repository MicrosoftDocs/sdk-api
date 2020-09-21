---
UID: NN:d2d1_1.ID2D1ImageBrush
title: ID2D1ImageBrush (d2d1_1.h)
description: Represents a brush based on an ID2D1Image.
helpviewer_keywords: ["ID2D1ImageBrush","ID2D1ImageBrush interface [Direct2D]","ID2D1ImageBrush interface [Direct2D]","described","d2d1_1/ID2D1ImageBrush","direct2d.id2d1imagebrush"]
old-location: direct2d\id2d1imagebrush.htm
tech.root: Direct2D
ms.assetid: c5088ce2-5744-4061-957b-25831478a714
ms.date: 12/05/2018
ms.keywords: ID2D1ImageBrush, ID2D1ImageBrush interface [Direct2D], ID2D1ImageBrush interface [Direct2D],described, d2d1_1/ID2D1ImageBrush, direct2d.id2d1imagebrush
req.header: d2d1_1.h
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ImageBrush
 - d2d1_1/ID2D1ImageBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.dll
api_name:
 - ID2D1ImageBrush
---

# ID2D1ImageBrush interface


## -description

Represents a brush based on an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1ImageBrush</b> interface inherits from <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>. <b>ID2D1ImageBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1ImageBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-getextendmodex">GetExtendModeX</a>
</td>
<td align="left" width="63%">
Gets the extend mode of the image brush on the x-axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-getextendmodey">GetExtendModeY</a>
</td>
<td align="left" width="63%">
Gets the extend mode of the image brush on the y-axis of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-getimage">GetImage</a>
</td>
<td align="left" width="63%">
Gets the image associated with the image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-getinterpolationmode">GetInterpolationMode</a>
</td>
<td align="left" width="63%">
Gets the interpolation mode of the image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-getsourcerectangle">GetSourceRectangle</a>
</td>
<td align="left" width="63%">
Gets the rectangle that will be used as the bounds of the image when drawn as an image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-setextendmodex">SetExtendModeX</a>
</td>
<td align="left" width="63%">
Sets how the content inside the source rectangle in the image brush will be extended on the x-axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-setextendmodey">SetExtendModeY</a>
</td>
<td align="left" width="63%">
Sets the extend mode on the y-axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-setimage">SetImage</a>
</td>
<td align="left" width="63%">
Sets the image associated with the provided image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-setinterpolationmode">SetInterpolationMode</a>
</td>
<td align="left" width="63%">
Sets the interpolation mode for the image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1imagebrush-setsourcerectangle">SetSourceRectangle</a>
</td>
<td align="left" width="63%">
Sets the source rectangle in the image brush.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>
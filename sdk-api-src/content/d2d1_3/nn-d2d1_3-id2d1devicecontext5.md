---
UID: NN:d2d1_3.ID2D1DeviceContext5
title: ID2D1DeviceContext5 (d2d1_3.h)
description: This interface performs all the same functions as the ID2D1DeviceContext4 interface, plus it enables the creation of color contexts and Svg documents.helpviewer_keywords: ["ID2D1DeviceContext5","ID2D1DeviceContext5 interface [Direct2D]","ID2D1DeviceContext5 interface [Direct2D]","described","d2d1_3/ID2D1DeviceContext5","direct2d.id2d1devicecontext5"]
old-location: direct2d\id2d1devicecontext5.htm
tech.root: Direct2D
ms.assetid: 38689191-3315-44F3-A259-DC1EB378485D
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext5, ID2D1DeviceContext5 interface [Direct2D], ID2D1DeviceContext5 interface [Direct2D],described, d2d1_3/ID2D1DeviceContext5, direct2d.id2d1devicecontext5
f1_keywords:
- d2d1_3/ID2D1DeviceContext5
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
- ID2D1DeviceContext5
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext5 interface


## -description


This interface performs all the same functions as the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a> interface, 
        plus it enables the creation of color contexts and Svg documents.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext5</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a>. <b>ID2D1DeviceContext5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DeviceContext5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace">CreateColorContextFromDxgiColorSpace</a>
</td>
<td align="left" width="63%">
Creates a color context from a DXGI color space type. It is only valid to use this with the Color Management Effect in 'Best' mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext5-createcolorcontextfromsimplecolorprofile-overload">CreateColorContextFromSimpleColorProfile</a>
</td>
<td align="left" width="63%">Overloaded. Creates a color context from a simple color profile. It is only valid to use this with the Color Management Effect in 'Best' mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument">CreateSvgDocument</a>
</td>
<td align="left" width="63%">
Creates an SVG document from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument">DrawSvgDocument</a>
</td>
<td align="left" width="63%">
Draws an SVG document.

</td>
</tr>
</table> 


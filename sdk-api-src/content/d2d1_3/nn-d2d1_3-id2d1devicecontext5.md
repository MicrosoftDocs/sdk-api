---
UID: NN:d2d1_3.ID2D1DeviceContext5
title: ID2D1DeviceContext5
author: windows-sdk-content
description: This interface performs all the same functions as the ID2D1DeviceContext4 interface, plus it enables the creation of color contexts and Svg documents.
old-location: direct2d\id2d1devicecontext5.htm
tech.root: direct2d
ms.assetid: 38689191-3315-44F3-A259-DC1EB378485D
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID2D1DeviceContext5, ID2D1DeviceContext5 interface [Direct2D], ID2D1DeviceContext5 interface [Direct2D],described, d2d1_3/ID2D1DeviceContext5, direct2d.id2d1devicecontext5
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext5 interface


## -description


This interface performs all the same functions as the <a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a> interface, 
        plus it enables the creation of color contexts and Svg documents.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext5</b> interface inherits from <a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a>. <b>ID2D1DeviceContext5</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/A8C785A1-0C16-4C16-9217-C54F1B911095">CreateColorContextFromDxgiColorSpace</a>
</td>
<td align="left" width="63%">
Creates a color context from a DXGI color space type. It is only valid to use this with the Color Management Effect in 'Best' mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f2cddce-1579-bd8f-3fc5-e993c3254230">CreateColorContextFromSimpleColorProfile</a>
</td>
<td align="left" width="63%">Overloaded. Creates a color context from a simple color profile. It is only valid to use this with the Color Management Effect in 'Best' mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B7965388-EFF0-40B4-AE00-3AB28DEA800B">CreateSvgDocument</a>
</td>
<td align="left" width="63%">
Creates an SVG document from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/369CB316-065D-41C6-8A1B-F41977EFA857">DrawSvgDocument</a>
</td>
<td align="left" width="63%">
Draws an SVG document.

</td>
</tr>
</table> 


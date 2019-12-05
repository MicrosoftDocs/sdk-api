---
UID: NN:d2d1_3.ID2D1DeviceContext6
title: ID2D1DeviceContext6 (d2d1_3.h)
description: This interface performs all the same functions as the existing ID2D1DeviceContext5 interface, plus it enables access to the BlendImage method.
old-location: direct2d\id2d1devicecontext6.htm
tech.root: Direct2D
ms.assetid: 474788F4-8AD7-4D5C-BF0B-9542E69620A9
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext6, ID2D1DeviceContext6 interface [Direct2D], ID2D1DeviceContext6 interface [Direct2D],described, d2d1_3/ID2D1DeviceContext6, direct2d.id2d1devicecontext6
ms.topic: interface
f1_keywords:
- d2d1_3/ID2D1DeviceContext6
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
- ID2D1DeviceContext6
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext6 interface


## -description


This interface performs all the same functions as the existing <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext5">ID2D1DeviceContext5</a> interface, 
        plus it enables access to the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext6-blendimage">BlendImage</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext6</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext5">ID2D1DeviceContext5</a>. <b>ID2D1DeviceContext6</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DeviceContext6</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext6-blendimage">BlendImage</a>
</td>
<td align="left" width="63%">
Draws an image to the device context using the specified blend mode. 
        Results are equivalent to using Direct2D's built-in <a href="https://docs.microsoft.com/windows/desktop/Direct2D/blend">Blend effect</a>.

</td>
</tr>
</table> 


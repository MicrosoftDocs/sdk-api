---
UID: NN:d2d1_3.ID2D1ColorContext1
title: ID2D1ColorContext1 (d2d1_3.h)
description: Represents a color context to be used with the Color Management Effect.
helpviewer_keywords: ["ID2D1ColorContext1","ID2D1ColorContext1 interface [Direct2D]","ID2D1ColorContext1 interface [Direct2D]","described","d2d1_3/ID2D1ColorContext1","direct2d.id2d1colorcontext1"]
old-location: direct2d\id2d1colorcontext1.htm
tech.root: Direct2D
ms.assetid: 77C8730B-C753-48E7-89C1-FBE28E687704
ms.date: 12/05/2018
ms.keywords: ID2D1ColorContext1, ID2D1ColorContext1 interface [Direct2D], ID2D1ColorContext1 interface [Direct2D],described, d2d1_3/ID2D1ColorContext1, direct2d.id2d1colorcontext1
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ColorContext1
 - d2d1_3/ID2D1ColorContext1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1ColorContext1
---

# ID2D1ColorContext1 interface


## -description

Represents a color context to be used with the Color Management Effect.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1ColorContext1</b> interface inherits from <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>. <b>ID2D1ColorContext1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1ColorContext1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1colorcontext1-getcolorcontexttype">GetColorContextType</a>
</td>
<td align="left" width="63%">
Retrieves the color context type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1colorcontext1-getdxgicolorspace">GetDXGIColorSpace</a>
</td>
<td align="left" width="63%">
Retrieves the DXGI color space of this context. Returns DXGI_COLOR_SPACE_CUSTOM when color context type is ICC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1colorcontext1-getsimplecolorprofile">GetSimpleColorProfile</a>
</td>
<td align="left" width="63%">
Retrieves a set simple color profile.

</td>
</tr>
</table>
---
UID: NF:directxmath.XMColorSRGBToRGB
title: XMColorSRGBToRGB function (directxmath.h)
description: Converts an sRGB color vector to RGB.
helpviewer_keywords: ["Use DirectX..XMColorSRGBToRGB","XMColorSRGBToRGB","XMColorSRGBToRGB method [DirectX Math Support APIs]","dxmath._xmcolorsrgbtorgb"]
old-location: dxmath\_xmcolorsrgbtorgb.htm
tech.root: dxmath
ms.assetid: A0F6AC87-AA83-4BF0-8259-577EABA72539
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorSRGBToRGB, XMColorSRGBToRGB, XMColorSRGBToRGB method [DirectX Math Support APIs], dxmath._xmcolorsrgbtorgb
req.header: directxmath.h
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
req.namespace: Use DirectX.
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMColorSRGBToRGB
 - directxmath/XMColorSRGBToRGB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMColorSRGBToRGB
---

# XMColorSRGBToRGB function


## -description

Converts an sRGB color vector to RGB.

## -parameters

### -param srgb

An sRGB color vector.

## -returns

Returns an <b>XMVECTOR</b> describing the converted RGBA color vector. The x element is red, the y element is green, the z element is blue, and the w element is the alpha value (which is a copy of srgb.w). Each element value has a range of 0.0 to 1.0 in the RGB colorspace.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcolorrgbtosrgb">XMColorRGBToSRGB</a>
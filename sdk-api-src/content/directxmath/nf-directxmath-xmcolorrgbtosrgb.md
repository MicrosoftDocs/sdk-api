---
UID: NF:directxmath.XMColorRGBToSRGB
title: XMColorRGBToSRGB function (directxmath.h)
description: Converts an RGB color vector to sRGB.
helpviewer_keywords: ["Use DirectX..XMColorRGBToSRGB","XMColorRGBToSRGB","XMColorRGBToSRGB method [DirectX Math Support APIs]","dxmath._xmcolorrgbtosrgb"]
old-location: dxmath\_xmcolorrgbtosrgb.htm
tech.root: dxmath
ms.assetid: ADD40A97-6BE1-4EDA-BBBB-6B186694F3E6
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorRGBToSRGB, XMColorRGBToSRGB, XMColorRGBToSRGB method [DirectX Math Support APIs], dxmath._xmcolorrgbtosrgb
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
 - XMColorRGBToSRGB
 - directxmath/XMColorRGBToSRGB
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
 - XMColorRGBToSRGB
---

# XMColorRGBToSRGB function


## -description

Converts an RGB color vector to sRGB.

## -parameters

### -param rgb

The original RGB color vector.

## -returns

Returns an <b>XMVECTOR</b> describing the converted sRGBA color vector. The x element is red, the y element is green, the z element is blue, and the w element is the alpha value (which is a copy of rgb.w). Each element value has a range of 0.0 to 1.0 in the sRGB colorspace.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcolorsrgbtorgb">XMColorSRGBToRGB</a>
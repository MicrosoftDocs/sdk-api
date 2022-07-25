---
UID: NF:directxmath.XMColorRGBToYUV_UHD
title: XMColorRGBToYUV_UHD function (directxmath.h)
description: Converts RGB color values to YUV UHD color values.
helpviewer_keywords: ["Use DirectX..XMColorRGBToYUV_UHD","XMColorRGBToYUV_UHD","XMColorRGBToYUV_UHD method [DirectX Math Support APIs]","dxmath.xmcolorrgbtoyuv_uhd"]
tech.root: dxmath
ms.date: 06/06/2021
ms.keywords: Use DirectX..XMColorRGBToYUV_UHD, XMColorRGBToYUV_UHD, XMColorRGBToYUV_UHD method [DirectX Math Support APIs], dxmath.xmcolorrgbtoyuv_uhd
req.header: directxmath.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
ms.custom: FE
f1_keywords:
 - XMColorRGBToYUV_UHD
 - directxmath/XMColorRGBToYUV_UHD
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
 - XMColorRGBToYUV_UHD
---

# XMColorRGBToYUV_UHD function


## -description

Converts RGB color values to YUV UHD color values.

## -parameters

### -param rgb [in]

Color value to convert. X element is Red, Y element is Green, Z element is Blue, and W element is Alpha. Each has a range of 0.0 to 1.0.

## -returns

 Returns the converted color value in Luma-Chrominance (YUV) aka YCbCr. The X element contains Luma (Y, 0.0 to 1.0), the Y element contains
       Blue-difference chroma (-0.5 to 0.5), the Z element contains the Red-difference chroma (-0.5 to 0.5), and the W element contains the Alpha (a copy of rgb.w).

## -remarks

 Converts using ITU-R BT.2020 W(r) = 0.2627 W(b) = 0.0-593 U(max) = 0.4351 V(max) = 0.6150.

> This function is new to DirectXMath 3.16

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcoloryuvtorgb_uhd">XMColorYUVToRGB_UHD</a>

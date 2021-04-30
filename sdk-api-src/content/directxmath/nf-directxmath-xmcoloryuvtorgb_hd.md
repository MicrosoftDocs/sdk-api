---
UID: NF:directxmath.XMColorYUVToRGB_HD
title: XMColorYUVToRGB_HD function (directxmath.h)
description: Converts YUV color values to RGB HD color values.
helpviewer_keywords: ["Use DirectX..XMColorYUVToRGB_HD","XMColorYUVToRGB_HD","XMColorYUVToRGB_HD method [DirectX Math Support APIs]","dxmath.xmcoloryuvtorgb_hd"]
old-location: dxmath\xmcoloryuvtorgb_hd.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorYUVToRGB_HD(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorYUVToRGB_HD, XMColorYUVToRGB_HD, XMColorYUVToRGB_HD method [DirectX Math Support APIs], dxmath.xmcoloryuvtorgb_hd
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
 - XMColorYUVToRGB_HD
 - directxmath/XMColorYUVToRGB_HD
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
 - XMColorYUVToRGB_HD
---

# XMColorYUVToRGB_HD function


## -description

Converts YUV color values to RGB HD color values.

## -parameters

### -param yuv [in]

Color value to convert in Luma-Chrominance (YUV) aka YCbCr. The X element contains Luma (Y, 0.0 to 1.0), the Y element 
        contains Blue-difference chroma (U, -0.5 to 0.5), the Z element contains the Red-difference chroma (V, -0.5 to 0.5), and the W element contains the Alpha (0.0 to 1.0).

## -returns

The converted color value. X element is Red, Y element is Green, Z element is Blue, and W element is Alpha (a copy of yuv.w). Each has a range of 0.0 to 1.0.

## -remarks

Converts using ITU-R BT.709 W(r) = 0.2126 W(b) = 0.0722 U(max) = 0.436 V(max) = 0.615.

<div class="alert"><b>Note</b>  <code>XMColorYUVToRGB_HD</code> is new for DirectXMath and is not available for XNAMath 2.x.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcolorrgbtoyuv_hd">XMColorRGBToYUV_HD</a>
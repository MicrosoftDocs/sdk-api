---
UID: NF:directxmath.XMColorRGBToYUV_HD
title: XMColorRGBToYUV_HD function (directxmath.h)
description: Converts RGB color values to YUV HD color values.
helpviewer_keywords: ["Use DirectX..XMColorRGBToYUV_HD","XMColorRGBToYUV_HD","XMColorRGBToYUV_HD method [DirectX Math Support APIs]","dxmath.xmcolorrgbtoyuv_hd"]
old-location: dxmath\xmcolorrgbtoyuv_hd.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorRGBToYUV_HD(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorRGBToYUV_HD, XMColorRGBToYUV_HD, XMColorRGBToYUV_HD method [DirectX Math Support APIs], dxmath.xmcolorrgbtoyuv_hd
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
 - XMColorRGBToYUV_HD
 - directxmath/XMColorRGBToYUV_HD
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
 - XMColorRGBToYUV_HD
---

# XMColorRGBToYUV_HD function


## -description

Converts RGB color values to YUV HD color values.

## -parameters

### -param rgb [in]

Color value to convert. X element is Red, Y element is Green, Z element is Blue, and W element is Alpha. Each has a range of 0.0 to 1.0.

## -returns

 Returns the converted color value in Luma-Chrominance (YUV) aka YCbCr. The X element contains Luma (Y, 0.0 to 1.0), the Y element contains 
       Blue-difference chroma (-0.5 to 0.5), the Z element contains the Red-difference chroma (-0.5 to 0.5), and the W element contains the Alpha (a copy of rgb.w).

## -remarks

 Converts using ITU-R BT.709 W(r) = 0.2126 W(b) = 0.0722 U(max) = 0.436 V(max) = 0.615.

<div class="alert"><b>Note</b>  <code>XMColorRGBToYUV_HD</code> is new for DirectXMath and is not available for XNAMath 2.x.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcoloryuvtorgb_hd">XMColorYUVToRGB_HD</a>
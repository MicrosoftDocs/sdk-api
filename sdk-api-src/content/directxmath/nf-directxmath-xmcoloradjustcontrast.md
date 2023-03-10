---
UID: NF:directxmath.XMColorAdjustContrast
title: XMColorAdjustContrast function (directxmath.h)
description: Adjusts the contrast value of a color.
helpviewer_keywords: ["Use DirectX..XMColorAdjustContrast","XMColorAdjustContrast","XMColorAdjustContrast method [DirectX Math Support APIs]","dxmath.xmcoloradjustcontrast"]
old-location: dxmath\xmcoloradjustcontrast.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorAdjustContrast(XMVECTOR,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorAdjustContrast, XMColorAdjustContrast, XMColorAdjustContrast method [DirectX Math Support APIs], dxmath.xmcoloradjustcontrast
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
 - XMColorAdjustContrast
 - directxmath/XMColorAdjustContrast
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
 - XMColorAdjustContrast
---

# XMColorAdjustContrast function


## -description

Adjusts the contrast value of a color.

## -parameters

### -param C [in]

<b>XMVECTOR</b> describing the color. Each of the components of <i>C</i> should be in the range 0.0f to 1.0f.

### -param Contrast [in]

Contrast value. This parameter linearly interpolates between 50 percent gray and the color <i>C</i>. If this
        parameter is 0.0f, the returned color is 50 percent gray. If this parameter is 1.0f, the returned color is the
        original color.

## -returns

Returns an <b>XMVECTOR</b> describing the color resulting from the contrast adjustment.

## -remarks

The following pseudocode demonstrates the operation of the function.


```
XMVECTOR colorOut;

colorOut.x = (C.x - 0.5f) * Contrast + 0.5f;
colorOut.y = (C.y - 0.5f) * Contrast + 0.5f;
colorOut.z = (C.z - 0.5f) * Contrast + 0.5f;
colorOut.w = C.w;

return colorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>
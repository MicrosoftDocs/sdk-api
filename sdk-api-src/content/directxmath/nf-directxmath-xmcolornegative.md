---
UID: NF:directxmath.XMColorNegative
title: XMColorNegative function (directxmath.h)
description: Determines the negative RGB color value of a color.
helpviewer_keywords: ["Use DirectX..XMColorNegative","XMColorNegative","XMColorNegative method [DirectX Math Support APIs]","dxmath.xmcolornegative"]
old-location: dxmath\xmcolornegative.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.color.XMColorNegative(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMColorNegative, XMColorNegative, XMColorNegative method [DirectX Math Support APIs], dxmath.xmcolornegative
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
 - XMColorNegative
 - directxmath/XMColorNegative
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
 - XMColorNegative
---

# XMColorNegative function


## -description

Determines the negative RGB color value of a color.

## -parameters

### -param C [in]

<b>XMVECTOR</b> describing the color. Each of the components of <i>C</i> should be in the range 0.0f to 1.0f.

## -returns

Returns an <b>XMVECTOR</b> describing the negative color. The w-component (alpha) is copied unmodified from the input vector.

## -remarks

The following pseudocode shows you the operation of the function.


```
XMVECTOR colorOut;

colorOut.x = 1.0f - C.x;
colorOut.y = 1.0f - C.y;
colorOut.z = 1.0f - C.z;
colorOut.w = C.w;

return colorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-color">DirectXMath Library Color Functions</a>
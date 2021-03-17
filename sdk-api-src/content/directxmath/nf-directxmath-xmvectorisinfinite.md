---
UID: NF:directxmath.XMVectorIsInfinite
title: XMVectorIsInfinite function (directxmath.h)
description: Performs a per-component test for +/- infinity on a vector.
helpviewer_keywords: ["Use DirectX..XMVectorIsInfinite","XMVectorIsInfinite","XMVectorIsInfinite method [DirectX Math Support APIs]","dxmath.xmvectorisinfinite"]
old-location: dxmath\xmvectorisinfinite.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVectorIsInfinite(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorIsInfinite, XMVectorIsInfinite, XMVectorIsInfinite method [DirectX Math Support APIs], dxmath.xmvectorisinfinite
req.header: directxmath.h
req.include-header: DirectXMath.h
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
 - XMVectorIsInfinite
 - directxmath/XMVectorIsInfinite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVectorIsInfinite
---

# XMVectorIsInfinite function


## -description

Performs a per-component test for +/- infinity on a vector.

## -parameters

### -param V [in]

Vector to test.

## -returns

Returns a vector containing the results of each component test.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = (V.x == +infinity || V.x == -infinity) ? 0xFFFFFFFF : 0;
Result.y = (V.y == +infinity || V.y == -infinity) ? 0xFFFFFFFF : 0;
Result.z = (V.z == +infinity || V.z == -infinity) ? 0xFFFFFFFF : 0;
Result.w = (V.w == +infinity || V.w == -infinity) ? 0xFFFFFFFF : 0;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-arithmetic">Vector Arithmetic Functions</a>
---
UID: NF:directxmath.XMVectorNearEqual
title: XMVectorNearEqual function (directxmath.h)
description: Performs a per-component test for equality of two vectors within a given threshold.
helpviewer_keywords: ["Use DirectX..XMVectorNearEqual","XMVectorNearEqual","XMVectorNearEqual method [DirectX Math Support APIs]","dxmath.xmvectornearequal"]
old-location: dxmath\xmvectornearequal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVectorNearEqual(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorNearEqual, XMVectorNearEqual, XMVectorNearEqual method [DirectX Math Support APIs], dxmath.xmvectornearequal
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
 - XMVectorNearEqual
 - directxmath/XMVectorNearEqual
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
 - XMVectorNearEqual
---

# XMVectorNearEqual function


## -description

Performs a per-component test for equality of two vectors within a given threshold.

## -parameters

### -param V1 [in]

First vector to compare.

### -param V2 [in]

Second vector compare.

### -param Epsilon [in]

Tolerance value used for judging equality.

## -returns

Returns a vector containing the results of each component test.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.x = (abs(V1.x - V2.x) <= Epsilon) ? 0xFFFFFFFF : 0;
Result.y = (abs(V1.y - V2.y) <= Epsilon) ? 0xFFFFFFFF : 0;
Result.z = (abs(V1.z - V2.z) <= Epsilon) ? 0xFFFFFFFF : 0;
Result.w = (abs(V1.w - V2.w) <= Epsilon) ? 0xFFFFFFFF : 0;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-comparison">Vector Comparison Functions</a>
---
UID: NF:directxmath.XMVectorHermite
title: XMVectorHermite function (directxmath.h)
description: Performs a Hermite spline interpolation, using the specified vectors. (XMVectorHermite)
helpviewer_keywords: ["Use DirectX..XMVectorHermite","XMVectorHermite","XMVectorHermite method [DirectX Math Support APIs]","dxmath.xmvectorhermite"]
old-location: dxmath\xmvectorhermite.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorHermite(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorHermite, XMVectorHermite, XMVectorHermite method [DirectX Math Support APIs], dxmath.xmvectorhermite
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
 - XMVectorHermite
 - directxmath/XMVectorHermite
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
 - XMVectorHermite
---

# XMVectorHermite function


## -description

Performs a Hermite spline interpolation, using the specified vectors.

## -parameters

### -param Position0 [in]

First position to interpolate from.

### -param Tangent0 [in]

Tangent vector for the first position.

### -param Position1 [in]

Second position to interpolate from.

### -param Tangent1 [in]

Tangent vector for the second position.

### -param t [in]

Interpolation control factor.

## -returns

Returns a vector containing the interpolation.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

float t2 = t * t;
float t3 = t2* t;

float P0 = 2.0f * t3 - 3.0f * t2 + 1.0f;
float T0 = t3 - 2.0f * t2 + t;
float P1 = -2.0f * t3 + 3.0f * t2;
float T1 = t3 - t2;

Result.x = P0 * Position0.x + T0 * Tangent0.x + P1 * Position1.x + T1 * Tangent1.x;
Result.y = P0 * Position0.y + T0 * Tangent0.y + P1 * Position1.y + T1 * Tangent1.y;
Result.z = P0 * Position0.z + T0 * Tangent0.z + P1 * Position1.z + T1 * Tangent1.z;
Result.w = P0 * Position0.w + T0 * Tangent0.w + P1 * Position1.w + T1 * Tangent1.w;

return Result;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-geometric">Geometric Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorhermitev">XMVectorHermiteV</a>

---
UID: NF:directxmath.XMVectorHermiteV
title: XMVectorHermiteV function (directxmath.h)
description: Performs a Hermite spline interpolation, using the specified vectors. (XMVectorHermiteV)
helpviewer_keywords: ["Use DirectX..XMVectorHermiteV","XMVectorHermiteV","XMVectorHermiteV method [DirectX Math Support APIs]","dxmath.xmvectorhermitev"]
old-location: dxmath\xmvectorhermitev.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorHermiteV(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorHermiteV, XMVectorHermiteV, XMVectorHermiteV method [DirectX Math Support APIs], dxmath.xmvectorhermitev
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
 - XMVectorHermiteV
 - directxmath/XMVectorHermiteV
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
 - XMVectorHermiteV
---

# XMVectorHermiteV function


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

### -param T [in]

Interpolating control factor with each component corresponding to a term of the Hermite equation.

## -returns

Returns a vector containing the interpolation.

## -remarks

This function is identical to <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorhermite">XMVectorHermite</a> except that independent weighting factors may be supplied in <i>T</i>. As an example, you might want to calculate two sets of Hermite spline interpolation, using the x and y-components of the position vectors for one set of 2D positions and the z and w-components of the position vectors for the other set of 2D positions. The x and y-components of <i>T</i> would determine the interpolation factors for the first Hermite spline interpolation. Similarly, the z and w-components of <i>T</i> would determine the interpolation factors for the second Hermite spline interpolation.

The following pseudocode demonstrates the operation of the function:


``` syntax

Result[i] = (2*(T.x)^3 - 3*(T.x)^2 + 1) * Position0.[i]
                  + ((T.y)^3 - 2*(T.y)^2 + (T.y)) * Tangent0.[i]
                  + (-2*(T.z)^3 + 3*(T.z)^2) * Position1.[i]
                  + ((T.w)^3 - *(T.w)^2) * Tangent1.[i]

```

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-geometric">Geometric Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorhermite">XMVectorHermite</a>

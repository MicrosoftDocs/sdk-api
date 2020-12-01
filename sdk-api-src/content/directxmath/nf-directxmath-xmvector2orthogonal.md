---
UID: NF:directxmath.XMVector2Orthogonal
title: XMVector2Orthogonal function (directxmath.h)
description: Computes a vector perpendicular to a 2D vector.
helpviewer_keywords: ["Use DirectX..XMVector2Orthogonal","XMVector2Orthogonal","XMVector2Orthogonal method [DirectX Math Support APIs]","dxmath.xmvector2orthogonal"]
old-location: dxmath\xmvector2orthogonal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector2Orthogonal(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2Orthogonal, XMVector2Orthogonal, XMVector2Orthogonal method [DirectX Math Support APIs], dxmath.xmvector2orthogonal
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
 - XMVector2Orthogonal
 - directxmath/XMVector2Orthogonal
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
 - XMVector2Orthogonal
---

# XMVector2Orthogonal function


## -description

Computes a vector perpendicular to a 2D vector.

## -parameters

### -param V [in]

2D vector.

## -returns

Returns the 2D vector orthogonal to <i>V</i>.

## -remarks

Note that a 'cross-product' in 2D is not well-defined. This function computes a generalized cross-product in 2D. 
    <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector2cross">XMVector2Cross</a> is another possible interpretation of a 'cross-product' in 2D.

The following pseudocode demonstrates the operation of the function:


```

XMVECTOR Result;

Result.x = -V.y;
Result.y = V.x;
Result.z = 0;
Result.w = 0;

return Result;

```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector2-geometric">DirectXMath Library 2D Vector Geometric Functions</a>
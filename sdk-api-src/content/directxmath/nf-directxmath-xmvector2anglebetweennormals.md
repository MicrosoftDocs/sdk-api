---
UID: NF:directxmath.XMVector2AngleBetweenNormals
title: XMVector2AngleBetweenNormals function (directxmath.h)
description: Computes the radian angle between two normalized 2D vectors.
helpviewer_keywords: ["Use DirectX..XMVector2AngleBetweenNormals","XMVector2AngleBetweenNormals","XMVector2AngleBetweenNormals method [DirectX Math Support APIs]","dxmath.xmvector2anglebetweennormals"]
old-location: dxmath\xmvector2anglebetweennormals.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector2AngleBetweenNormals(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2AngleBetweenNormals, XMVector2AngleBetweenNormals, XMVector2AngleBetweenNormals method [DirectX Math Support APIs], dxmath.xmvector2anglebetweennormals
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
 - XMVector2AngleBetweenNormals
 - directxmath/XMVector2AngleBetweenNormals
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
 - XMVector2AngleBetweenNormals
---

# XMVector2AngleBetweenNormals function


## -description

Computes the radian angle between two normalized 2D vectors.

## -parameters

### -param N1 [in]

Normalized 2D vector.

### -param N2 [in]

Normalized 2D vector.

## -returns

Returns a vector. The radian angle between <i>N1</i> and <i>N2</i> is replicated to each of the components.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector2-geometric">DirectXMath Library 2D Vector Geometric Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector2anglebetweennormalsest">XMVector2AngleBetweenNormalsEst</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector2anglebetweenvectors">XMVector2AngleBetweenVectors</a>
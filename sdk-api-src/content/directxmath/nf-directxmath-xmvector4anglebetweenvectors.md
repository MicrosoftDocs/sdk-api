---
UID: NF:directxmath.XMVector4AngleBetweenVectors
title: XMVector4AngleBetweenVectors function (directxmath.h)
description: Compute the radian angle between two 4D vectors.
helpviewer_keywords: ["Use DirectX..XMVector4AngleBetweenVectors","XMVector4AngleBetweenVectors","XMVector4AngleBetweenVectors method [DirectX Math Support APIs]","dxmath.xmvector4anglebetweenvectors"]
old-location: dxmath\xmvector4anglebetweenvectors.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4AngleBetweenVectors(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4AngleBetweenVectors, XMVector4AngleBetweenVectors, XMVector4AngleBetweenVectors method [DirectX Math Support APIs], dxmath.xmvector4anglebetweenvectors
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
 - XMVector4AngleBetweenVectors
 - directxmath/XMVector4AngleBetweenVectors
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
 - XMVector4AngleBetweenVectors
---

# XMVector4AngleBetweenVectors function


## -description

Compute the radian angle between two 4D vectors.

## -parameters

### -param V1 [in]

4D vector.

### -param V2 [in]

4D vector.

## -returns

Returns a vector. The radian angle between <i>V1</i> and <i>V2</i> is replicated to each of the components.

## -remarks

If V1 and V2 are normalized 4D vectors, it is faster to use <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4anglebetweennormals">XMVector4AngleBetweenNormals</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-geometric">DirectXMath Library 4D Vector Geometric Functions</a>
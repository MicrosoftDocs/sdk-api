---
UID: NF:directxmath.XMVector3Transform
title: XMVector3Transform function (directxmath.h)
description: Transforms a 3D vector by a matrix.
helpviewer_keywords: ["Use DirectX..XMVector3Transform","XMVector3Transform","XMVector3Transform method [DirectX Math Support APIs]","dxmath.xmvector3transform"]
old-location: dxmath\xmvector3transform.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3Transform(XMVECTOR,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3Transform, XMVector3Transform, XMVector3Transform method [DirectX Math Support APIs], dxmath.xmvector3transform
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
 - XMVector3Transform
 - directxmath/XMVector3Transform
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
 - XMVector3Transform
---

# XMVector3Transform function


## -description

Transforms a 3D vector by a matrix.

## -parameters

### -param V [in]

3D vector.

### -param M [in]

Transformation matrix.

## -returns

Returns the transformed vector.

## -remarks

<code>XMVector3Transform</code> ignores the w component of the input vector, and uses a value of 1 instead. The w component of the returned vector may be non-homogeneous (!= 1.0).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-transformation">DirectXMath Library 3D Vector Transformation Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector3transformstream">XMVector3TransformStream</a>
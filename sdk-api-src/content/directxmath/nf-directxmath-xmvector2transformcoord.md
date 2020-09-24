---
UID: NF:directxmath.XMVector2TransformCoord
title: XMVector2TransformCoord function (directxmath.h)
description: Transforms a 2D vector by a given matrix, projecting the result back into w = 1.
helpviewer_keywords: ["Use DirectX..XMVector2TransformCoord","XMVector2TransformCoord","XMVector2TransformCoord method [DirectX Math Support APIs]","dxmath.xmvector2transformcoord"]
old-location: dxmath\xmvector2transformcoord.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector2TransformCoord(XMVECTOR,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2TransformCoord, XMVector2TransformCoord, XMVector2TransformCoord method [DirectX Math Support APIs], dxmath.xmvector2transformcoord
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
 - XMVector2TransformCoord
 - directxmath/XMVector2TransformCoord
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
 - XMVector2TransformCoord
---

# XMVector2TransformCoord function


## -description

Transforms a 2D vector by a given matrix, projecting the result back into w = 1.

## -parameters

### -param V [in]

2D vector.

### -param M [in]

Transformation matrix.

## -returns

Returns the transformed vector.

## -remarks

<code>XMVector2TransformCoord</code> performs transformations by using the input matrix row 0 and row 1 for rotation and scaling, 
    and row 3 for translation (effectively assuming row 2 is 0).  The w component of the input vector is assumed to be 1.0. 
    The z component of the returned vector should be ignored and its w component will have a value of 1.0.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector2-transformation">DirectXMath Library 2D Vector Transformation Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector2transformcoordstream">XMVector2TransformCoordStream</a>
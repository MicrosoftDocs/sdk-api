---
UID: NF:directxmath.XMVector3TransformCoord
title: XMVector3TransformCoord function (directxmath.h)
description: Transforms a 3D vector by a given matrix, projecting the result back into w = 1.
helpviewer_keywords: ["Use DirectX..XMVector3TransformCoord","XMVector3TransformCoord","XMVector3TransformCoord method [DirectX Math Support APIs]","dxmath.xmvector3transformcoord"]
old-location: dxmath\xmvector3transformcoord.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3TransformCoord(XMVECTOR,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3TransformCoord, XMVector3TransformCoord, XMVector3TransformCoord method [DirectX Math Support APIs], dxmath.xmvector3transformcoord
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
 - XMVector3TransformCoord
 - directxmath/XMVector3TransformCoord
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
 - XMVector3TransformCoord
---

# XMVector3TransformCoord function


## -description

Transforms a 3D vector by a given matrix, projecting the result back into w = 1.

## -parameters

### -param V [in]

3D vector.

### -param M [in]

Transformation matrix.

## -returns

Returns the transformed vector.

## -remarks

<code>XMVector3TransformCoord</code> ignores the w component of the input vector, and uses a value of 1.0 instead. The w component of the returned vector will always be 1.0.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-transformation">DirectXMath Library 3D Vector Transformation Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector3transformcoordstream">XMVector3TransformCoordStream</a>
---
UID: NF:directxmath.XMVector3InverseRotate
title: XMVector3InverseRotate function (directxmath.h)
description: Rotates a 3D vector using the inverse of a quaternion.
helpviewer_keywords: ["Use DirectX..XMVector3InverseRotate","XMVector3InverseRotate","XMVector3InverseRotate method [DirectX Math Support APIs]","dxmath.xmvector3inverserotate"]
old-location: dxmath\xmvector3inverserotate.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3InverseRotate(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3InverseRotate, XMVector3InverseRotate, XMVector3InverseRotate method [DirectX Math Support APIs], dxmath.xmvector3inverserotate
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
 - XMVector3InverseRotate
 - directxmath/XMVector3InverseRotate
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
 - XMVector3InverseRotate
---

# XMVector3InverseRotate function


## -description

Rotates a 3D vector using the inverse of a quaternion.

## -parameters

### -param V [in]

3D vector to rotate.

### -param RotationQuaternion [in]

Quaternion that describes the inverse of the  rotation to apply to the vector.

## -returns

Returns the rotated 3D vector.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-transformation">DirectXMath Library 3D Vector Transformation Functions</a>
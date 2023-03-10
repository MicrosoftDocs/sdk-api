---
UID: NF:directxmath.XMQuaternionRotationAxis
title: XMQuaternionRotationAxis function (directxmath.h)
description: Computes a rotation quaternion about an axis.
helpviewer_keywords: ["Use DirectX..XMQuaternionRotationAxis","XMQuaternionRotationAxis","XMQuaternionRotationAxis method [DirectX Math Support APIs]","dxmath.xmquaternionrotationaxis"]
old-location: dxmath\xmquaternionrotationaxis.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionRotationAxis(XMVECTOR,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionRotationAxis, XMQuaternionRotationAxis, XMQuaternionRotationAxis method [DirectX Math Support APIs], dxmath.xmquaternionrotationaxis
req.header: directxmath.h
req.include-header: 
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
 - XMQuaternionRotationAxis
 - directxmath/XMQuaternionRotationAxis
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMQuaternionRotationAxis
---

# XMQuaternionRotationAxis function


## -description

Computes a rotation quaternion about an axis.

## -parameters

### -param Axis [in]

3D vector describing the axis of rotation.

### -param Angle [in]

Angle of rotation in radians. Angles are measured clockwise when looking along the rotation axis toward the origin.

## -returns

Returns the rotation quaternion.

## -remarks

The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

If <i>Axis</i> is a normalized vector, it is faster to use
   <a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionrotationnormal">XMQuaternionRotationNormal</a>


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>
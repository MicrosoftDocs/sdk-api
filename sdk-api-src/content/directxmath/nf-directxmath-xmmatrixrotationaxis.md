---
UID: NF:directxmath.XMMatrixRotationAxis
title: XMMatrixRotationAxis function (directxmath.h)
description: Builds a matrix that rotates around an arbitrary axis.
helpviewer_keywords: ["Use DirectX..XMMatrixRotationAxis","XMMatrixRotationAxis","XMMatrixRotationAxis method [DirectX Math Support APIs]","dxmath.xmmatrixrotationaxis"]
old-location: dxmath\xmmatrixrotationaxis.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixRotationAxis(XMVECTOR,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixRotationAxis, XMMatrixRotationAxis, XMMatrixRotationAxis method [DirectX Math Support APIs], dxmath.xmmatrixrotationaxis
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
 - XMMatrixRotationAxis
 - directxmath/XMMatrixRotationAxis
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
 - XMMatrixRotationAxis
---

# XMMatrixRotationAxis function


## -description

Builds a matrix that rotates around an arbitrary axis.

## -parameters

### -param Axis [in]

Vector describing the axis of rotation.

### -param Angle [in]

Angle of rotation in radians. Angles are measured clockwise when looking along the rotation axis toward the origin.

## -returns

Returns the rotation matrix.

## -remarks

If <i>Axis</i> is a normalized vector, it is faster to use the  <a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrixrotationnormal">XMMatrixRotationNormal</a> function to build this type of matrix.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>
---
UID: NF:directxmath.XMMatrixTransformation2D
title: XMMatrixTransformation2D function (directxmath.h)
description: Builds a 2D transformation matrix in the xy plane.
helpviewer_keywords: ["Use DirectX..XMMatrixTransformation2D","XMMatrixTransformation2D","XMMatrixTransformation2D method [DirectX Math Support APIs]","dxmath.xmmatrixtransformation2d"]
old-location: dxmath\xmmatrixtransformation2d.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixTransformation2D(XMVECTOR,float,XMVECTOR,XMVECTOR,float,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixTransformation2D, XMMatrixTransformation2D, XMMatrixTransformation2D method [DirectX Math Support APIs], dxmath.xmmatrixtransformation2d
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
 - XMMatrixTransformation2D
 - directxmath/XMMatrixTransformation2D
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
 - XMMatrixTransformation2D
---

# XMMatrixTransformation2D function


## -description

Builds a 2D transformation matrix in the xy plane.

## -parameters

### -param ScalingOrigin [in]

2D vector describing the center of the scaling.

### -param ScalingOrientation [in]

Scaling rotation factor.

### -param Scaling [in]

2D vector containing the scaling factors for the x-axis and y-axis.

### -param RotationOrigin [in]

2D vector describing the center of the rotation.

### -param Rotation [in]

Angle of rotation, in radians.

### -param Translation [in]

2D vector describing the translation.

## -returns

Returns the transformation matrix.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>
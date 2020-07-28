---
UID: NF:directxmath.XMMatrixAffineTransformation2D
title: XMMatrixAffineTransformation2D function (directxmath.h)
description: Builds a 2D affine transformation matrix in the xy plane.
helpviewer_keywords: ["Use DirectX..XMMatrixAffineTransformation2D","XMMatrixAffineTransformation2D","XMMatrixAffineTransformation2D method [DirectX Math Support APIs]","dxmath.xmmatrixaffinetransformation2d"]
old-location: dxmath\xmmatrixaffinetransformation2d.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixAffineTransformation2D(XMVECTOR,XMVECTOR,float,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMatrixAffineTransformation2D, XMMatrixAffineTransformation2D, XMMatrixAffineTransformation2D method [DirectX Math Support APIs], dxmath.xmmatrixaffinetransformation2d
f1_keywords:
- directxmath/XMMatrixAffineTransformation2D
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectXMath.h
api_name:
- XMMatrixAffineTransformation2D
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMMatrixAffineTransformation2D function


## -description


Builds a 2D affine transformation matrix in the xy plane. 


## -parameters




### -param Scaling [in]

2D vector of scaling factors for the x-coordinate and y-coordinate.


### -param RotationOrigin [in]

2D vector describing the center of rotation.


### -param Rotation [in]

Radian angle of rotation.


### -param Translation [in]

2D vector translation offsets.


## -returns



Returns the 2D affine transformation matrix.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-matrix">DirectXMath Library Matrix Functions</a>
 

 


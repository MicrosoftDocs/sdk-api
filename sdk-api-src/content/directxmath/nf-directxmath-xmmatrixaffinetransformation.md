---
UID: NF:directxmath.XMMatrixAffineTransformation
title: XMMatrixAffineTransformation function (directxmath.h)
author: windows-sdk-content
description: Builds an affine transformation matrix.
old-location: dxmath\xmmatrixaffinetransformation.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.matrix.XMMatrixAffineTransformation(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMMatrixAffineTransformation, XMMatrixAffineTransformation, XMMatrixAffineTransformation method [DirectX Math Support APIs], dxmath.xmmatrixaffinetransformation
ms.topic: function
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
 - XMMatrixAffineTransformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMMatrixAffineTransformation function


## -description


Builds an affine transformation matrix.


## -parameters




### -param Scaling [in]

Vector of scaling factors for each dimension.


### -param RotationOrigin [in]

Point identifying the center of rotation.


### -param RotationQuaternion [in]

Rotation factors.


### -param Translation [in]

Translation offsets.


## -returns



Returns the affine transformation matrix, built from the scaling, rotation, and translation information.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/d59d0dcc-deae-3f7e-55c5-0c5ff383343b">DirectXMath Library Matrix Functions</a>
 

 


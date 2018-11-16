---
UID: NF:directxmath.XMVector2Transform
title: XMVector2Transform function
author: windows-sdk-content
description: Transforms a 2D vector by a matrix.
old-location: dxmath\xmvector2transform.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector2Transform(XMVECTOR,XMMATRIX)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMVector2Transform, XMVector2Transform, XMVector2Transform method [DirectX Math Support APIs], dxmath.xmvector2transform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVector2Transform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector2Transform
: 
---

# XMVector2Transform function


## -description


Transforms a 2D vector by a matrix.


## -parameters




### -param V [in]

2D vector.


### -param M [in]

Transformation matrix.


## -returns



Returns the transformed vector.




## -remarks



<code>XMVector2Transform</code> performs transformations by using the input matrix rows 0 and 1 for rotation and scaling, and row 3 for 
    translation (effectively assuming row 2 is 0).  The w component of the input vector is assumed to be 0.
    The z component of the output vector should be ignored and its w component may be non-homogeneous (!= 1.0).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/175c2073-40ac-06b5-2f0e-495bd74b1502">DirectXMath Library 2D Vector Transformation Functions</a>



<a href="https://msdn.microsoft.com/5499b128-4425-476d-8998-c58078b0f33e">XMVector2TransformStream</a>
 

 


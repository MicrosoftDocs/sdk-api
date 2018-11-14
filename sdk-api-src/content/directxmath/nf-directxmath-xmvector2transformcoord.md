---
UID: NF:directxmath.XMVector2TransformCoord
title: XMVector2TransformCoord function
author: windows-sdk-content
description: Transforms a 2D vector by a given matrix, projecting the result back into w = 1.
old-location: dxmath\xmvector2transformcoord.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector2TransformCoord(XMVECTOR,XMMATRIX)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVector2TransformCoord, XMVector2TransformCoord, XMVector2TransformCoord method [DirectX Math Support APIs], dxmath.xmvector2transformcoord
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
 - XMVector2TransformCoord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector2TransformCoord
: 
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




<a href="https://msdn.microsoft.com/175c2073-40ac-06b5-2f0e-495bd74b1502">DirectXMath Library 2D Vector Transformation Functions</a>



<a href="https://msdn.microsoft.com/2c7c1c16-3ab4-4619-beb2-9464f70cfd1b">XMVector2TransformCoordStream</a>
 

 


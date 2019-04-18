---
UID: NF:directxmath.XMPlaneTransform
title: XMPlaneTransform function (directxmath.h)
author: windows-sdk-content
description: Transforms a plane by a given matrix.
old-location: dxmath\xmplanetransform.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneTransform(XMVECTOR,XMMATRIX)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneTransform, XMPlaneTransform, XMPlaneTransform method [DirectX Math Support APIs], dxmath.xmplanetransform
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
 - XMPlaneTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMPlaneTransform function


## -description


Transforms a plane by a given matrix.


## -parameters




### -param P [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.


### -param M [in]

Transformation matrix.


## -returns



Returns the transformed plane as a 4D vector whose components are the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6505e72e-4af5-5db3-4fc0-f83fa77692b1">DirectXMath Library Plane Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404689(v=VS.85).aspx">XMPlaneTransformStream</a>
 

 


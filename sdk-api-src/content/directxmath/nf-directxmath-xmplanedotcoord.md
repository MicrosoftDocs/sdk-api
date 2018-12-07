---
UID: NF:directxmath.XMPlaneDotCoord
title: XMPlaneDotCoord function
author: windows-sdk-content
description: Calculates the dot product between an input plane and a 3D vector.
old-location: dxmath\xmplanedotcoord.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneDotCoord(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMPlaneDotCoord, XMPlaneDotCoord, XMPlaneDotCoord method [DirectX Math Support APIs], dxmath.xmplanedotcoord
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - XMPlaneDotCoord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMPlaneDotCoord function


## -description


Calculates the dot product between an input plane and a 3D vector.


## -parameters




### -param P [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation 


```
XMVECTOR vectorOut;

vectorOut.x = P.x * V.x + P.y * V.y + P.z * V.z + P.w * 1.0f;
vectorOut.y = P.x * V.x + P.y * V.y + P.z * V.z + P.w * 1.0f;
vectorOut.z = P.x * V.x + P.y * V.y + P.z * V.z + P.w * 1.0f;
vectorOut.w = P.x * V.x + P.y * V.y + P.z * V.z + P.w * 1.0f;

return vectorOut;
```

.


### -param V [in]

3D vector to use in the dot product. The w component of <i>V</i> is always treated as if is 1.0f.


## -returns



Returns the dot product between <i>P</i> and <i>V</i> replicated into each of the four components of the
       returned <b>XMVECTOR</b>.




## -remarks



This function can be useful in finding the signed distance from a point to a plane. The following pseudocode
   demonstrates the operation of the function.

<code>Ax+By+Cz+D=0</code>

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6505e72e-4af5-5db3-4fc0-f83fa77692b1">DirectXMath Library Plane Functions</a>
 

 


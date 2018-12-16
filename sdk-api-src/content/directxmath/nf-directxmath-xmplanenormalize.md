---
UID: NF:directxmath.XMPlaneNormalize
title: XMPlaneNormalize function
author: windows-sdk-content
description: Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.
old-location: dxmath\xmplanenormalize.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneNormalize(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMPlaneNormalize, XMPlaneNormalize, XMPlaneNormalize method [DirectX Math Support APIs], dxmath.xmplanenormalize
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
 - XMPlaneNormalize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMPlaneNormalize function


## -description


Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.


## -parameters




### -param P [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation 


```
XMVECTOR Result;

float LengthSq = P.x * P.x + P.y * P.y + P.z * P.z;

float ReciprocalLength = 1.0f / sqrt(LengthSq);
Result.x = P.x * ReciprocalLength;
Result.y = P.y * ReciprocalLength;
Result.z = P.z * ReciprocalLength;
Result.w = P.w * ReciprocalLength;

return Result;
```

.


## -returns



Returns the normalized plane as a 4D vector whose components are the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.




## -remarks



The following pseudocode demonstrates the operation of the function:

<code>Ax+By+Cz+D=0</code>

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6505e72e-4af5-5db3-4fc0-f83fa77692b1">DirectXMath Library Plane Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee420149(v=VS.85).aspx">XMPlaneNormalizeEst</a>
 

 


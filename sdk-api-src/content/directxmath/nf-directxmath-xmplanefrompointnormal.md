---
UID: NF:directxmath.XMPlaneFromPointNormal
title: XMPlaneFromPointNormal function
author: windows-sdk-content
description: Computes the equation of a plane constructed from a point in the plane and a normal vector.
old-location: dxmath\xmplanefrompointnormal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneFromPointNormal(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMPlaneFromPointNormal, XMPlaneFromPointNormal, XMPlaneFromPointNormal method [DirectX Math Support APIs], dxmath.xmplanefrompointnormal
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
 - XMPlaneFromPointNormal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMPlaneFromPointNormal
: 
---

# XMPlaneFromPointNormal function


## -description


Computes the equation of a plane constructed from a point in the plane and a normal vector.


## -parameters




### -param Point [in]

3D vector describing a point in the plane.


### -param Normal [in]

3D vector normal to the plane.


## -returns



Returns a vector whose components are the coefficients of the plane (A, B, C, D) for the plane equation
       <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR Result;

Result.x = Normal.x;
Result.y = Normal.y;
Result.z = Normal.z;
Result.w = -(Point.x * Normal.x + Point.y * Normal.y + Point.z * Normal.z);

return Result;</pre>
</td>
</tr>
</table></span></div>.




## -remarks



The following pseudocode demonstrates the operation of the function:

<code>Ax+By+Cz+D=0</code>

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6505e72e-4af5-5db3-4fc0-f83fa77692b1">DirectXMath Library Plane Functions</a>
 

 


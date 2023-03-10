---
UID: NF:directxmath.XMPlaneDotNormal
title: XMPlaneDotNormal function (directxmath.h)
description: Calculates the dot product between the normal vector of a plane and a 3D vector.
helpviewer_keywords: ["Use DirectX..XMPlaneDotNormal","XMPlaneDotNormal","XMPlaneDotNormal method [DirectX Math Support APIs]","dxmath.xmplanedotnormal"]
old-location: dxmath\xmplanedotnormal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneDotNormal(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneDotNormal, XMPlaneDotNormal, XMPlaneDotNormal method [DirectX Math Support APIs], dxmath.xmplanedotnormal
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
 - XMPlaneDotNormal
 - directxmath/XMPlaneDotNormal
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
 - XMPlaneDotNormal
---

# XMPlaneDotNormal function


## -description

Calculates the dot product between the normal vector of a plane and a 3D vector.

## -parameters

### -param P [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation 


```
XMVECTOR vectorOut;

vectorOut.x = P.x * V.x + P.y * V.y + P.z * V.z;
vectorOut.y = P.x * V.x + P.y * V.y + P.z * V.z;
vectorOut.z = P.x * V.x + P.y * V.y + P.z * V.z;
vectorOut.w = P.x * V.x + P.y * V.y + P.z * V.z;

return vectorOut;
```

.

### -param V [in]

3D vector to use in the dot product. The w component of <i>V</i> is always treated as if is 0.0f.

## -returns

Returns the dot product between the normal vector of the plane and <i>V</i> replicated into each of the four
       components of the returned <b>XMVECTOR</b>.

## -remarks

This function is useful for calculating the angle between the normal vector of the plane, and another normal vector. The
   following pseudocode demonstrates the operation of the function.

<code>Ax+By+Cz+D=0</code>

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-plane">DirectXMath Library Plane Functions</a>
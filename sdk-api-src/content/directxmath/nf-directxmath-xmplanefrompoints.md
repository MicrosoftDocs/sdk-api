---
UID: NF:directxmath.XMPlaneFromPoints
title: XMPlaneFromPoints function (directxmath.h)
description: Computes the equation of a plane constructed from three points in the plane.
helpviewer_keywords: ["Use DirectX..XMPlaneFromPoints","XMPlaneFromPoints","XMPlaneFromPoints method [DirectX Math Support APIs]","dxmath.xmplanefrompoints"]
old-location: dxmath\xmplanefrompoints.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneFromPoints(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneFromPoints, XMPlaneFromPoints, XMPlaneFromPoints method [DirectX Math Support APIs], dxmath.xmplanefrompoints
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
 - XMPlaneFromPoints
 - directxmath/XMPlaneFromPoints
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
 - XMPlaneFromPoints
---

# XMPlaneFromPoints function


## -description

Computes the equation of a plane constructed from three points in the plane.

## -parameters

### -param Point1 [in]

3D vector describing a point in the plane.

### -param Point2 [in]

3D vector describing a point in the plane.

### -param Point3 [in]

3D vector describing a point in the plane.

## -returns

Returns a vector whose components are the coefficients of the plane (A, B, C, D) for the plane equation
       


```
XMVECTOR Result;
XMVECTOR N;
XMVECTOR D;

XMVECTOR V21 = XMVectorSubtract(Point1, Point2);
XMVECTOR V31 = XMVectorSubtract(Point1, Point3);

N = XMVector3Cross(V21, V31);
N = XMVector3Normalize(N);

D = XMPlaneDotNormal(N, Point1);

Result.x = N.x;
Result.y = N.y;
Result.z = N.z;
Result.w = -D.w;

return Result;
```

.

## -remarks

The following pseudocode demonstrates the operation of the function:

<code>Ax+By+Cz+D=0</code>

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-plane">DirectXMath Library Plane Functions</a>
---
UID: NF:directxmath.XMPlaneIntersectPlane
title: XMPlaneIntersectPlane function (directxmath.h)
description: Finds the intersection of two planes.
helpviewer_keywords: ["Use DirectX..XMPlaneIntersectPlane","XMPlaneIntersectPlane","XMPlaneIntersectPlane method [DirectX Math Support APIs]","dxmath.xmplaneintersectplane"]
old-location: dxmath\xmplaneintersectplane.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneIntersectPlane(XMVECTOR@,XMVECTOR@,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneIntersectPlane, XMPlaneIntersectPlane, XMPlaneIntersectPlane method [DirectX Math Support APIs], dxmath.xmplaneintersectplane
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
 - XMPlaneIntersectPlane
 - directxmath/XMPlaneIntersectPlane
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
 - XMPlaneIntersectPlane
---

# XMPlaneIntersectPlane function


## -description

Finds the intersection of two planes.

## -parameters

### -param pLinePoint1 [out]

Address of a 3D vector describing one point on the line of intersection. See remarks.

### -param pLinePoint2 [out]

Address of a 3D vector describing a second point on the line of intersection. See remarks.

### -param P1 [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.

### -param P2 [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.

## -returns

None.

## -remarks

If the planes are parallel to one another, all components of the returned point vectors are equal to QNaN.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-plane">DirectXMath Library Plane Functions</a>
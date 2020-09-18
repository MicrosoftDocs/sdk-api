---
UID: NF:directxmath.XMPlaneIntersectLine
title: XMPlaneIntersectLine function (directxmath.h)
description: Finds the intersection between a plane and a line.
helpviewer_keywords: ["Use DirectX..XMPlaneIntersectLine","XMPlaneIntersectLine","XMPlaneIntersectLine method [DirectX Math Support APIs]","dxmath.xmplaneintersectline"]
old-location: dxmath\xmplaneintersectline.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneIntersectLine(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneIntersectLine, XMPlaneIntersectLine, XMPlaneIntersectLine method [DirectX Math Support APIs], dxmath.xmplaneintersectline
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
 - XMPlaneIntersectLine
 - directxmath/XMPlaneIntersectLine
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
 - XMPlaneIntersectLine
---

# XMPlaneIntersectLine function


## -description

Finds the intersection between a plane and a line.

## -parameters

### -param P [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.

### -param LinePoint1 [in]

3D vector describing the first point on the line.

### -param LinePoint2 [in]

3D vector describing the second point on the line.

## -returns

Returns the intersection of the plane <i>P</i> and the line defined by <i>LinePoint1</i> and
       <i>LinePoint2</i>. If the line is parallel to the plane, all components of the returned vector are equal to
       QNaN.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-plane">DirectXMath Library Plane Functions</a>
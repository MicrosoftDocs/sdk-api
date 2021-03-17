---
UID: NF:directxmath.XMVector2IntersectLine
title: XMVector2IntersectLine function (directxmath.h)
description: Finds the intersection of two lines.
helpviewer_keywords: ["Use DirectX..XMVector2IntersectLine","XMVector2IntersectLine","XMVector2IntersectLine method [DirectX Math Support APIs]","dxmath.xmvector2intersectline"]
old-location: dxmath\xmvector2intersectline.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector2IntersectLine(XMVECTOR,XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2IntersectLine, XMVector2IntersectLine, XMVector2IntersectLine method [DirectX Math Support APIs], dxmath.xmvector2intersectline
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMVector2IntersectLine
 - directxmath/XMVector2IntersectLine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVector2IntersectLine
---

# XMVector2IntersectLine function


## -description

Finds the intersection of two lines.

## -parameters

### -param Line1Point1 [in]

2D vector describing the first point on the first line.

### -param Line1Point2 [in]

2D vector describing a second point on the first line.

### -param Line2Point1 [in]

2D vector describing the first point on the second line.

### -param Line2Point2 [in]

2D vector describing a second point on the second line.

## -returns

Returns the intersection point. If the lines are parallel, the returned vector will be a NaN. If the two lines are coincident, the returned vector will be positive infinity.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector2-geometric">DirectXMath Library 2D Vector Geometric Functions</a>
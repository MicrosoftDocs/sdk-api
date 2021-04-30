---
UID: NS:directxcollision.BoundingFrustum
title: BoundingFrustum
description: A bounding frustum object.
helpviewer_keywords: ["BoundingFrustum","BoundingFrustum structure [DirectX Math Support APIs]","directxcollision/BoundingFrustum","dxmath.boundingfrustum"]
old-location: dxmath\boundingfrustum.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.directxmath.BoundingFrustum
ms.date: 12/05/2018
ms.keywords: BoundingFrustum, BoundingFrustum structure [DirectX Math Support APIs], directxcollision/BoundingFrustum, dxmath.boundingfrustum
req.header: directxcollision.h
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
req.namespace: 
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
 - BoundingFrustum
 - directxcollision/BoundingFrustum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectXCollision.h
api_name:
 - BoundingFrustum
---

## -description

A bounding frustum object.

## -struct-fields

### -field CORNER_COUNT

The number of corners defining the <b>BoundingFrustum</b>.

### -field Origin

The origin of the <b>BoundingFrustum</b>.

### -field Orientation

The orientation of the <b>BoundingFrustum</b> represented as a quaternion.

### -field RightSlope

The slope of the right side of the <b>BoundingFrustum</b>.

### -field LeftSlope

The slope of the left side of the <b>BoundingFrustum</b>.

### -field TopSlope

The slope of the top of the <b>BoundingFrustum</b>.

### -field BottomSlope

The slope of the bottom of the <b>BoundingFrustum</b>.

### -field Near

The distance of the near plane of the <b>BoundingFrustum</b> from its origin.

### -field Far

The distance of the far plane from the origin of the <b>BoundingFrustum</b>.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-directxmath-classes">DirectXMath Library Classes</a>
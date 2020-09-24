---
UID: NS:directxcollision.BoundingOrientedBox
title: BoundingOrientedBox
description: An oriented bounding box object.
helpviewer_keywords: ["BoundingOrientedBox","BoundingOrientedBox structure [DirectX Math Support APIs]","directxcollision/BoundingOrientedBox","dxmath.boundingorientedbox"]
old-location: dxmath\boundingorientedbox.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.directxmath.BoundingOrientedBox
ms.date: 12/05/2018
ms.keywords: BoundingOrientedBox, BoundingOrientedBox structure [DirectX Math Support APIs], directxcollision/BoundingOrientedBox, dxmath.boundingorientedbox
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
 - BoundingOrientedBox
 - directxcollision/BoundingOrientedBox
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
 - BoundingOrientedBox
---

## -description

An oriented bounding box object.

## -struct-fields

### -field CORNER_COUNT

The number of points defining the <b>BoundingOrientedBox</b>.

### -field Center

The center of the <b>BoundingOrientedBox</b>.

### -field Extents

The extents of the <b>BoundingOrientedBox</b>.

### -field Orientation

The orientation of the <b>BoundingOrientedBox</b> represented as a quaternion.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-directxmath-classes">DirectXMath Library Classes</a>
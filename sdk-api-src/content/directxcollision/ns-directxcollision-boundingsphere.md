---
UID: NS:directxcollision.BoundingSphere
title: BoundingSphere
description: A bounding sphere object.
helpviewer_keywords: ["BoundingSphere","BoundingSphere structure [DirectX Math Support APIs]","directxcollision/BoundingSphere","dxmath.boundingsphere"]
old-location: dxmath\boundingsphere.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.directxcollision.BoundingSphere
ms.date: 12/05/2018
ms.keywords: BoundingSphere, BoundingSphere structure [DirectX Math Support APIs], directxcollision/BoundingSphere, dxmath.boundingsphere
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
 - BoundingSphere
 - directxcollision/BoundingSphere
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
 - BoundingSphere
---

# BoundingSphere structure


## -description

A bounding sphere object.

## -struct-fields

### -field Center

The center of the <b>BoundingSphere</b>.

### -field Radius

The radius of the <b>BoundingSphere</b>.

### -field operator=

TBD

### -field BoundingSphere

Creates an instance of the **BoundingSphere** class.

### -field Transform

Transforms the <b>BoundingSphere</b>

### -field Contains

Tests whether the <b>BoundingSphere</b> contains a specified object.

### -field Intersects

Tests the <b>BoundingSphere</b> for intersection with an object.

### -field ContainedBy

Tests whether the <b>BoundingSphere</b> is contained by the specified frustum.

### -field CreateMerged

Creates a <b>BoundingSphere</b> that contains the two specified <b>BoundingSphere</b> objects.

### -field CreateFromBoundingBox

Creates a <b>BoundingSphere</b> containing the specified [BoundingBox](/windows/win32/api/directxcollision/ns-directxcollision-boundingbox).

### -field CreateFromPoints

Creates a new <b>BoundingSphere</b> from a list of points.

### -field CreateFromFrustum

TBD 




##### - DirectX.BoundingSphere

Creates an instance of the <b>BoundingSphere</b> class.


#### - op_Assignment

Initializes the <b>BoundingSphere</b> with values from a specified <b>BoundingSphere</b>

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-directxmath-classes">DirectXMath Library Classes</a>


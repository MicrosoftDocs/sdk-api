---
UID: NS:directxcollision.BoundingBox
title: BoundingBox
description: A bounding axis-aligned object.helpviewer_keywords: ["BoundingBox","BoundingBox structure [DirectX Math Support APIs]","directxcollision/BoundingBox","dxmath.boundingbox"]
old-location: dxmath\boundingbox.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.directxcollision.BoundingBox
ms.date: 12/05/2018
ms.keywords: BoundingBox, BoundingBox structure [DirectX Math Support APIs], directxcollision/BoundingBox, dxmath.boundingbox
f1_keywords:
- directxcollision/BoundingBox
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectXCollision.h
api_name:
- BoundingBox
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BoundingBox structure


## -description


A bounding axis-aligned object.


## -struct-fields




### -field CORNER_COUNT

The number of points defining the BoundingBox.


### -field Center

The center of the BoundingBox.


### -field Extents

The extents of the BoundingBox.


### -field operator=

TBD 


### -field BoundingBox

Creates an instance of the <code>BoundingBox</code> class.


### -field Transform

Transforms the BoundingBox.


### -field GetCorners

Retrieves the corners of the BoundingBox.


### -field Contains

Tests whether the BoundingBox contains a specified object.


### -field Intersects

Tests the BoundingBox for intersection with another object.


### -field ContainedBy

Tests whether the <b>BoundingBox</b> is contained by the specified frustum.


### -field CreateMerged

Creates a BoundingBox large enough to contains two specified BoundBox intances.


### -field CreateFromSphere

Creates a BoundingBox large enough to contain the a specified BoundingSphere.


### -field CreateFromPoints

Creates a BoundingBox from points.


#### - op_Assignment

Copies values from another BoundingBox.


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

Use DirectX.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-directxmath-classes">DirectXMath Library Classes</a>
 

 


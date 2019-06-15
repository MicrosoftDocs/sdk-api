---
UID: NS:directxcollision.BoundingOrientedBox
title: BoundingOrientedBox
author: windows-sdk-content
description: An oriented bounding box object.
old-location: dxmath\boundingorientedbox.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.directxmath.BoundingOrientedBox
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BoundingOrientedBox, BoundingOrientedBox structure [DirectX Math Support APIs], directxcollision/BoundingOrientedBox, dxmath.boundingorientedbox
ms.topic: struct
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
 - BoundingOrientedBox
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BoundingOrientedBox structure


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


### -field operator=

TBD 


### -field BoundingOrientedBox

Creates an instance of <b>BoundingOrientedBox</b>.


### -field Transform

Transforms the <b>BoundingOrientedBox</b>.


### -field GetCorners

Retrieves the corners of the <b>BoundingOrientedBox</b>.


### -field Contains

Tests whether the <b>BoundingOrientedBox</b> contains another object.


### -field Intersects

Tests the <b>BoundingOrientedBox</b> for intersection with another object.


### -field ContainedBy

Tests whether the <b>BoundingOrientedBox</b> is contained by a frustum.


### -field CreateFromBoundingBox

Creates a <b>BoundingOrientedBox</b> from a <a href="https://msdn.microsoft.com/8dac1c63-2eb6-4ad2-8495-593c4927391f">BoundingBox</a>.


### -field CreateFromPoints

Creates a <b>BoundingOrientedBox</b> from a collection of points.


#### - op_Assignment

Copies values from another <b>BoundingOrientedBox</b>.


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-directxmath-classes">DirectXMath Library Classes</a>
 

 


---
UID: NS:directxcollision.BoundingBox
title: BoundingBox
author: windows-sdk-content
description: A bounding axis-aligned object.
old-location: dxmath\boundingbox.htm
old-project: dxmath
ms.assetid: T:Microsoft.directx_sdk.directxcollision.BoundingBox
ms.author: windowssdkdev
ms.date: 04/23/2018
ms.keywords: BoundingBox, BoundingBox structure [DirectX Math Support APIs], directxcollision/BoundingBox, dxmath.boundingbox
ms.prod: windows
ms.technology: windows-sdk
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
req.namespace: DirectX::TriangleTests
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	DirectXCollision.h
api_name:
-	BoundingBox
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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


#### - BoundingBox

Creates an instance of the <code>BoundingBox</code> class.


#### - ContainedBy

Tests whether the <b>BoundingBox</b> is contained by the specified frustum.


#### - Contains

Tests whether the BoundingBox contains a specified object.


#### - CreateFromPoints

Creates a BoundingBox from points.


#### - CreateFromSphere

Creates a BoundingBox large enough to contain the a specified BoundingSphere.


#### - CreateMerged

Creates a BoundingBox large enough to contains two specified BoundBox intances.


#### - GetCorners

Retrieves the corners of the BoundingBox.


#### - Intersects

Tests the BoundingBox for intersection with another object.


#### - Transform

Transforms the BoundingBox.


#### - op_Assignment

Copies values from another BoundingBox.


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

Use DirectX.




## -see-also




<a href="https://msdn.microsoft.com/e50e24ab-24f2-d59e-22a4-aaf7015d0255">DirectXMath Library Classes</a>
 

 


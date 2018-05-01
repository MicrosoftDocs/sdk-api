---
UID: NE:gdiplusenums.PathPointType
title: PathPointType
author: windows-driver-content
description: The PathPointType enumeration indicates point types and flags for the data points in a path.
old-location: gdiplus\_gdiplus_ENUM_PathPointType.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\pathpointtype.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: PathPointType, PathPointType enumeration [GDI+], PathPointTypeBezier, PathPointTypeBezier3, PathPointTypeCloseSubpath, PathPointTypeLine, PathPointTypePathDashMode, PathPointTypePathMarker, PathPointTypePathTypeMask, PathPointTypeStart, _gdiplus_ENUM_PathPointType, gdiplus._gdiplus_ENUM_PathPointType, gdiplusenums/PathPointType, gdiplusenums/PathPointTypeBezier, gdiplusenums/PathPointTypeBezier3, gdiplusenums/PathPointTypeCloseSubpath, gdiplusenums/PathPointTypeLine, gdiplusenums/PathPointTypePathDashMode, gdiplusenums/PathPointTypePathMarker, gdiplusenums/PathPointTypePathTypeMask, gdiplusenums/PathPointTypeStart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdiplusenums.h
api_name:
-	PathPointType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# PathPointType enumeration


## -description


The <b>PathPointType</b> enumeration indicates point types and flags for the data points in a path. Bits 0 through 2 indicate the type of a point, and bits 3 through 7 hold a set of flags that specify attributes of a point. This enumeration is used by the <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>, <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff568848">PathData</a> classes.


## -enum-fields




### -field PathPointTypeStart

Indicates that the point is the start of a figure. 


### -field PathPointTypeLine

Indicates that the point is one of the two endpoints of a line. 


### -field PathPointTypeBezier

Indicates that the point is an endpoint or control point of a cubic Bézier spline. 


### -field PathPointTypePathTypeMask

Masks all bits except for the three low-order bits, which indicate the point type. 


### -field PathPointTypeDashMode


### -field PathPointTypePathMarker

Specifies that the point is a marker. 


### -field PathPointTypeCloseSubpath

Specifies that the point is the last point in a closed subpath (figure). 


### -field PathPointTypeBezier3

Indicates that the point is an endpoint or control point of a cubic Bézier spline. 


#### - PathPointTypePathDashMode

Not used. 


## -remarks



A <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points.




## -see-also




<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568848">PathData</a>
 

 


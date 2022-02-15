---
UID: NE:gdiplusenums.PathPointType
title: PathPointType (gdiplusenums.h)
description: The PathPointType enumeration indicates point types and flags for the data points in a path.
helpviewer_keywords: ["PathPointType","PathPointType enumeration [GDI+]","PathPointTypeBezier","PathPointTypeBezier3","PathPointTypeCloseSubpath","PathPointTypeLine","PathPointTypePathDashMode","PathPointTypePathMarker","PathPointTypePathTypeMask","PathPointTypeStart","_gdiplus_ENUM_PathPointType","gdiplus._gdiplus_ENUM_PathPointType","gdiplusenums/PathPointType","gdiplusenums/PathPointTypeBezier","gdiplusenums/PathPointTypeBezier3","gdiplusenums/PathPointTypeCloseSubpath","gdiplusenums/PathPointTypeLine","gdiplusenums/PathPointTypePathDashMode","gdiplusenums/PathPointTypePathMarker","gdiplusenums/PathPointTypePathTypeMask","gdiplusenums/PathPointTypeStart"]
old-location: gdiplus\_gdiplus_ENUM_PathPointType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\pathpointtype.htm
ms.date: 12/05/2018
ms.keywords: PathPointType, PathPointType enumeration [GDI+], PathPointTypeBezier, PathPointTypeBezier3, PathPointTypeCloseSubpath, PathPointTypeLine, PathPointTypePathDashMode, PathPointTypePathMarker, PathPointTypePathTypeMask, PathPointTypeStart, _gdiplus_ENUM_PathPointType, gdiplus._gdiplus_ENUM_PathPointType, gdiplusenums/PathPointType, gdiplusenums/PathPointTypeBezier, gdiplusenums/PathPointTypeBezier3, gdiplusenums/PathPointTypeCloseSubpath, gdiplusenums/PathPointTypeLine, gdiplusenums/PathPointTypePathDashMode, gdiplusenums/PathPointTypePathMarker, gdiplusenums/PathPointTypePathTypeMask, gdiplusenums/PathPointTypeStart
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - PathPointType
 - gdiplusenums/PathPointType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - PathPointType
---

## -description

The <b>PathPointType</b> enumeration indicates point types and flags for the data points in a path. Bits 0 through 2 indicate the type of a point, and bits 3 through 7 hold a set of flags that specify attributes of a point. This enumeration is used by the <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>, <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>, and <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a> classes.

## -enum-fields

### -field PathPointTypeStart:0

Indicates that the point is the start of a figure.

### -field PathPointTypeLine:1

Indicates that the point is one of the two endpoints of a line.

### -field PathPointTypeBezier:3

Indicates that the point is an endpoint or control point of a cubic Bézier spline.

### -field PathPointTypePathTypeMask:0x07

Masks all bits except for the three low-order bits, which indicate the point type.

### -field PathPointTypeDashMode:0x10

Not used.

### -field PathPointTypePathMarker:0x20

Specifies that the point is a marker.

### -field PathPointTypeCloseSubpath:0x80

Specifies that the point is the last point in a closed subpath (figure).

### -field PathPointTypeBezier3:3

Indicates that the point is an endpoint or control point of a cubic Bézier spline. 

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points.

## -see-also

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a>

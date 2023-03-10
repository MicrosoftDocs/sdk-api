---
UID: NF:gdipluspath.GraphicsPath.GraphicsPath(constPoint,constBYTE,INT,FillMode)
title: GraphicsPath::GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode) (gdipluspath.h)
description: Creates a GraphicsPath::GraphicsPath object based on an array of points, an array of types, and a fill mode. (overload 2/2)
helpviewer_keywords: ["GraphicsPath","GraphicsPath class [GDI+]","GraphicsPath constructor","GraphicsPath constructor [GDI+]","GraphicsPath constructor [GDI+]","GraphicsPath class","GraphicsPath.GraphicsPath","GraphicsPath.GraphicsPath(IN const Point","IN const BYTE","IN INT","IN FillMode)","GraphicsPath.GraphicsPath(const Point*","const BYTE*","INT","FillMode)","GraphicsPath::GraphicsPath","GraphicsPath::GraphicsPath(IN const Point","IN const BYTE","IN INT","IN FillMode)","_gdiplus_CLASS_GraphicsPath_GraphicsPath_Point_points_BYTE_types_INT_count_FillMode_fillMode_","gdiplus._gdiplus_CLASS_GraphicsPath_GraphicsPath_Point_points_BYTE_types_INT_count_FillMode_fillMode_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GraphicsPath_Point_points_BYTE_types_INT_count_FillMode_fillMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathconstructors\graphicspath_46pointpoints_bytetypes_intcount_fillmod.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath, GraphicsPath class [GDI+],GraphicsPath constructor, GraphicsPath constructor [GDI+], GraphicsPath constructor [GDI+],GraphicsPath class, GraphicsPath.GraphicsPath, GraphicsPath.GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode), GraphicsPath.GraphicsPath(const Point*,const BYTE*,INT,FillMode), GraphicsPath::GraphicsPath, GraphicsPath::GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode), _gdiplus_CLASS_GraphicsPath_GraphicsPath_Point_points_BYTE_types_INT_count_FillMode_fillMode_, gdiplus._gdiplus_CLASS_GraphicsPath_GraphicsPath_Point_points_BYTE_types_INT_count_FillMode_fillMode_
req.header: gdipluspath.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - GraphicsPath::GraphicsPath
 - gdipluspath/GraphicsPath::GraphicsPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.GraphicsPath
---

# GraphicsPath::GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode)


## -description

Creates a <b>GraphicsPath::GraphicsPath</b> object based on an array of points, an array of types, and a fill mode.

## -parameters

### -param points [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of points that specifies the endpoints and control points of the lines and Bezier splines that are used to draw the path.

### -param types [in]

Type: <b>const BYTE*</b>

Pointer to an array of bytes that holds the point type and a set of flags for each point in the 
					<i>points</i> array. The point type is stored in the three least significant bits, and the flags are stored in the four most significant bits. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. This is the same as the number of elements in the 
					<i>types</i> array.

### -param fillMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a> enumeration that specifies how areas are filled if the path intersects itself. The default value is FillModeAlternate.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-graphicspath(constgraphicspath_)">GraphicsPath Constructors</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>

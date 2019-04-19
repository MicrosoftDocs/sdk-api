---
UID: NF:gdipluspath.GraphicsPath.GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode)
title: GraphicsPath::GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode) (gdipluspath.h)
author: windows-sdk-content
description: Creates a GraphicsPath::GraphicsPath object based on an array of points, an array of types, and a fill mode.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GraphicsPath_Point_points_BYTE_types_INT_count_FillMode_fillMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathconstructors\graphicspath_46pointpoints_bytetypes_intcount_fillmod.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GraphicsPath, GraphicsPath class [GDI+],GraphicsPath constructor, GraphicsPath constructor [GDI+], GraphicsPath constructor [GDI+],GraphicsPath class, GraphicsPath.GraphicsPath, GraphicsPath.GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode), GraphicsPath.GraphicsPath(const Point*,const BYTE*,INT,FillMode), GraphicsPath::GraphicsPath, GraphicsPath::GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode), _gdiplus_CLASS_GraphicsPath_GraphicsPath_Point_points_BYTE_types_INT_count_FillMode_fillMode_, gdiplus._gdiplus_CLASS_GraphicsPath_GraphicsPath_Point_points_BYTE_types_INT_count_FillMode_fillMode_
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.GraphicsPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GraphicsPath::GraphicsPath(IN const Point,IN const BYTE,IN INT,IN FillMode)


## -description


Creates a <b>GraphicsPath::GraphicsPath</b> object based on an array of points, an array of types, and a fill mode.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>*</b>

Pointer to an array of points that specifies the endpoints and control points of the lines and Bezier splines that are used to draw the path. 


### -param types [in]

Type: <b>const BYTE*</b>

Pointer to an array of bytes that holds the point type and a set of flags for each point in the 
					<i>points</i> array. The point type is stored in the three least significant bits, and the flags are stored in the four most significant bits. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a> enumeration. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. This is the same as the number of elements in the 
					<i>types</i> array. 


### -param fillMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534120(v=VS.85).aspx">FillMode</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534120(v=VS.85).aspx">FillMode</a> enumeration that specifies how areas are filled if the path intersects itself. The default value is FillModeAlternate. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534120(v=VS.85).aspx">FillMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535523(v=VS.85).aspx">GraphicsPath Constructors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534481(v=VS.85).aspx">PathData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>
 

 


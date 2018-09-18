---
UID: NF:gdipluspath.GraphicsPath.GraphicsPath(IN const PointF,IN const BYTE,IN INT,IN FillMode)
title: GraphicsPath::GraphicsPath(IN const PointF,IN const BYTE,IN INT,IN FillMode)
author: windows-sdk-content
description: Creates a GraphicsPath::GraphicsPath object based on an array of points, an array of types, and a fill mode.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GraphicsPath_PointF_points_BYTE_types_INT_count_FillMode_fillMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathconstructors\graphicspath_97pointfpoints_bytetypes_intcount_fillmo.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: GraphicsPath, GraphicsPath class [GDI+],GraphicsPath constructor, GraphicsPath constructor [GDI+], GraphicsPath constructor [GDI+],GraphicsPath class, GraphicsPath.GraphicsPath, GraphicsPath.GraphicsPath(IN const PointF,IN const BYTE,IN INT,IN FillMode), GraphicsPath.GraphicsPath(const PointF*,const BYTE*,INT,FillMode), GraphicsPath::GraphicsPath, GraphicsPath::GraphicsPath(IN const PointF,IN const BYTE,IN INT,IN FillMode), _gdiplus_CLASS_GraphicsPath_GraphicsPath_PointF_points_BYTE_types_INT_count_FillMode_fillMode_, gdiplus._gdiplus_CLASS_GraphicsPath_GraphicsPath_PointF_points_BYTE_types_INT_count_FillMode_fillMode_
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# GraphicsPath::GraphicsPath(IN const PointF,IN const BYTE,IN INT,IN FillMode)


## -description


Creates a <b>GraphicsPath::GraphicsPath</b> object based on an array of points, an array of types, and a fill mode.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of points that specifies the endpoints and control points of the lines and Bezier splines that are used to draw the path. 


### -param types [in]

Type: <b>const BYTE*</b>

Pointer to an array of bytes that holds the point type and a set of flags for each point in the 
					<i>points</i> array. The point type is stored in the three least significant bits, and the flags are stored in the four most significant bits. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a> enumeration. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. This is the same as the number of elements in the 
					<i>types</i> array. 


### -param fillMode [in]

Type: <b><a href="https://msdn.microsoft.com/fd54e07b-74a2-4bce-9fa3-e36afec4be92">FillMode</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/fd54e07b-74a2-4bce-9fa3-e36afec4be92">FillMode</a> enumeration that specifies how areas are filled if the path intersects itself. The default value is <code>FillModeAlternate</code>. 


## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/fd54e07b-74a2-4bce-9fa3-e36afec4be92">FillMode</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/933dd879-480c-4b8a-965a-1656382d849a">GraphicsPath Constructors</a>



<a href="https://msdn.microsoft.com/b8e9a4cb-72e1-4646-956a-50801176a3bd">PathData</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>
 

 


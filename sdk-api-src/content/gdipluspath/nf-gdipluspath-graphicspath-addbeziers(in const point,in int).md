---
UID: NF:gdipluspath.GraphicsPath.AddBeziers(IN const Point,IN INT)
title: GraphicsPath::AddBeziers(IN const Point,IN INT)
author: windows-sdk-content
description: The GraphicsPath::AddBeziers method adds a sequence of connected B&#233;zier splines to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddbeziersmethods\addbeziers_6pointfpoints_intcount.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: AddBeziers, AddBeziers method [GDI+], AddBeziers method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddBeziers method, GraphicsPath.AddBeziers, GraphicsPath.AddBeziers(IN const Point,IN INT), GraphicsPath.AddBeziers(const PointF*,INT), GraphicsPath::AddBeziers, GraphicsPath::AddBeziers(IN const Point,IN INT), _gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_
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
 - GraphicsPath.AddBeziers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddBeziers(IN const Point,IN INT)


## -description


The <b>GraphicsPath::AddBeziers</b> method adds a sequence of connected Bézier splines to the current figure of this path.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of starting points, ending points, and control points for the connected splines. The first spline is constructed from the first point through the fourth point in the array and uses the second and third points as control points. Each subsequent spline in the sequence needs exactly three more points: the ending point of the previous spline is used as the starting point, the next two points in the sequence are control points, and the third point is the ending point. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1c4f3d1b-1fdb-4fde-8f69-bcfac1a33663">AddBezier Methods</a>



<a href="https://msdn.microsoft.com/fb754409-1867-41bd-a9d3-952e393490f8">AddBeziers Methods</a>



<a href="https://msdn.microsoft.com/81f43f7e-a383-44f7-a3bd-2969d541b616">AddCurve Methods</a>



<a href="https://msdn.microsoft.com/3ee279ea-20cc-4089-b1a5-13bf1c7c4942">Bézier Splines</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/af19e82b-0d13-4fb0-981e-8d5dd1bbfb36">Drawing Bézier Splines</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>
 

 


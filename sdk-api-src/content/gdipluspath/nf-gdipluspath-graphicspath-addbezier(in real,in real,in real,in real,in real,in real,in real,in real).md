---
UID: NF:gdipluspath.GraphicsPath.AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
title: GraphicsPath::AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
author: windows-sdk-content
description: The GraphicsPath::AddBezier method adds a B&#233;zier spline to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddBezier_REAL_x1_REAL_y1_REAL_x2_REAL_y2_REAL_x3_REAL_y3_REAL_x4_REAL_y.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddbeziermethods\addbezier_43realx1_realy1_realx2_realy2_realx3_rea.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: AddBezier, AddBezier method [GDI+], AddBezier method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddBezier method, GraphicsPath.AddBezier, GraphicsPath.AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), GraphicsPath.AddBezier(REAL,REAL,REAL,REAL,REAL,REAL,REAL,REAL), GraphicsPath::AddBezier, GraphicsPath::AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_GraphicsPath_AddBezier_REAL_x1_REAL_y1_REAL_x2_REAL_y2_REAL_x3_REAL_y3_REAL_x4_REAL_y, gdiplus._gdiplus_CLASS_GraphicsPath_AddBezier_REAL_x1_REAL_y1_REAL_x2_REAL_y2_REAL_x3_REAL_y3_REAL_x4_REAL_y
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
 - GraphicsPath.AddBezier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddBezier(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>GraphicsPath::AddBezier</b> method adds a Bézier spline to the current figure of this path.


## -parameters




### -param x1 [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the starting point of the Bézier spline. 


### -param y1 [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the starting point of the Bézier spline. 


### -param x2 [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the first control point of the Bézier spline. 


### -param y2 [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the first control point of the Bézier spline. 


### -param x3 [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the second control point of the Bézier spline. 


### -param y3 [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the second control point of the Bézier spline. 


### -param x4 [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the ending point of the Bézier spline. 


### -param y4 [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the ending point of the Bézier spline. 


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
 

 


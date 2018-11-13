---
UID: NF:gdipluspath.GraphicsPath.AddPolygon(IN const PointF,IN INT)
title: GraphicsPath::AddPolygon(IN const PointF,IN INT)
author: windows-sdk-content
description: The GraphicsPath::AddPolygon method adds a polygon to this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddPolygon_PointF_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddpolygonmethods\addpolygon_35pointfpoints_intcount.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: AddPolygon, AddPolygon method [GDI+], AddPolygon method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddPolygon method, GraphicsPath.AddPolygon, GraphicsPath.AddPolygon(IN const PointF,IN INT), GraphicsPath.AddPolygon(const PointF*,INT), GraphicsPath::AddPolygon, GraphicsPath::AddPolygon(IN const PointF,IN INT), _gdiplus_CLASS_GraphicsPath_AddPolygon_PointF_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddPolygon_PointF_points_INT_count_
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
 - GraphicsPath.AddPolygon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddPolygon(IN const PointF,IN INT)


## -description


The <b>GraphicsPath::AddPolygon</b> method adds a polygon to this path.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of points that specifies the vertices of the polygon. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The <b>GraphicsPath::AddPolygon</b> method is similar to the <b>AddLines</b> method. The difference is that a polygon is an intrinsically closed figure, but a sequence of lines is not a closed figure unless you call <a href="https://msdn.microsoft.com/8f828820-7dd6-4dd0-959c-4dcfb1ca6ac7">GraphicsPath::CloseFigure</a>. When Windows GDI+ renders a path, each polygon in that path is closed; that is, the last vertex of the polygon is connected to the first vertex by a straight line.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object <i>path</i>, adds a polygon to <i>path</i>, and then draws <i>path</i>.


```cpp
VOID Example_AddPolygon(HDC hdc)
{
   Graphics graphics(hdc); 

   PointF pts[] = {PointF(20.0f, 20.0f),
                   PointF(120.0f, 20.0f),
                   PointF(120.0f, 70.0f)};

   GraphicsPath path;
   path.AddPolygon(pts, 3);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```





## -see-also




<a href="https://msdn.microsoft.com/c768a38e-0b64-4254-b844-ade567eaea8f">AddPolygon Methods</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>



<a href="https://msdn.microsoft.com/f1155341-83f3-4805-8d42-a1910515db31">Polygons</a>
 

 


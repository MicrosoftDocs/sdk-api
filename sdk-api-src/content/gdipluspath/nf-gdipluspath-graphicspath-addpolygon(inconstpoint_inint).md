---
UID: NF:gdipluspath.GraphicsPath.AddPolygon(IN const Point,IN INT)
title: GraphicsPath::AddPolygon(IN const Point,IN INT) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::AddPolygon method adds a polygon to this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddPolygon_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddpolygonmethods\addpolygon.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddPolygon, AddPolygon method [GDI+], AddPolygon method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddPolygon method, GraphicsPath.AddPolygon, GraphicsPath.AddPolygon(IN const Point,IN INT), GraphicsPath.AddPolygon(const Point*,INT), GraphicsPath::AddPolygon, GraphicsPath::AddPolygon(IN const Point,IN INT), _gdiplus_CLASS_GraphicsPath_AddPolygon_Point_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddPolygon_Point_points_INT_count_
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
ms.custom: 19H1
---

# GraphicsPath::AddPolygon(IN const Point,IN INT)


## -description


The <b>GraphicsPath::AddPolygon</b> method adds a polygon to this path.


## -parameters




### -param points [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of points that specifies the vertices of the polygon. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



The <b>GraphicsPath::AddPolygon</b> method is similar to the <b>AddLines</b> method. The difference is that a polygon is an intrinsically closed figure, but a sequence of lines is not a closed figure unless you call <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-closefigure">GraphicsPath::CloseFigure</a>. When Windows GDI+ renders a path, each polygon in that path is closed; that is, the last vertex of the polygon is connected to the first vertex by a straight line.


#### Examples



The following example creates a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object <i>path</i>, adds a polygon to <i>path</i>, and then draws <i>path</i>.


```cpp
VOID Example_AddPolygon(HDC hdc)
{
   Graphics graphics(hdc); 
 
   Point pts[] = {Point(20, 20),
                  Point(120, 20),
                  Point(120, 70)};

   GraphicsPath path;
   path.AddPolygon(pts, 3);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpoint_inint)">AddPolygon Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-polygons-about">Polygons</a>
 

 


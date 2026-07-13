---
UID: NF:gdipluspath.GraphicsPath.GetPointCount
title: GraphicsPath::GetPointCount (gdipluspath.h)
description: The GraphicsPath::GetPointCount method gets the number of points in this path's array of data points. This is the same as the number of types in the path's array of point types.
helpviewer_keywords: ["GetPointCount","GetPointCount method [GDI+]","GetPointCount method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","GetPointCount method","GraphicsPath.GetPointCount","GraphicsPath::GetPointCount","_gdiplus_CLASS_GraphicsPath_GetPointCount_","gdiplus._gdiplus_CLASS_GraphicsPath_GetPointCount_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPointCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getpointcount.htm
ms.date: 12/05/2018
ms.keywords: GetPointCount, GetPointCount method [GDI+], GetPointCount method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPointCount method, GraphicsPath.GetPointCount, GraphicsPath::GetPointCount, _gdiplus_CLASS_GraphicsPath_GetPointCount_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPointCount_
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
 - GraphicsPath::GetPointCount
 - gdipluspath/GraphicsPath::GetPointCount
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
 - GraphicsPath.GetPointCount
---

# GraphicsPath::GetPointCount


## -description

The <b>GraphicsPath::GetPointCount</b> method gets the number of points in this path's array of data points. This is the same as the number of types in the path's array of point types.



## -returns

Type: <b>INT</b>

This method returns the number of points in the path's array of data points.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.


#### Examples



The following example creates a path that has one ellipse and one line. The code calls the <b>GraphicsPath::GetPointCount</b> method to determine the number of data points stored in the path. Then the code calls the <a href="/previous-versions/ms535581(v=vs.85)">GraphicsPath::GetPathPoints</a> method to retrieve those data points. Finally, the code fills a small ellipse at each of the data points.


```cpp
VOID GetPointCountExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has one ellipse and one line.
   GraphicsPath path;
   path.AddEllipse(10, 10, 200, 100);
   path.AddLine(220, 120, 300, 160);

   // Find out how many data points are stored in the path.
   INT count = path.GetPointCount();

   // Draw the path points.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   PointF* points = new PointF[count];
   path.GetPathPoints(points, count);

   for(INT j = 0; j < count; ++j)
      graphics.FillEllipse(
         &redBrush, 
         points[j].X - 3.0f, 
         points[j].Y - 3.0f, 
         6.0f, 
         6.0f); 

   delete [] points; 
} 
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)">GetPathPoints Methods</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GraphicsPath::GetPathData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GraphicsPath::GetPathTypes</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

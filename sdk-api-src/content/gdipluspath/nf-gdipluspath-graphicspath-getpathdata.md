---
UID: NF:gdipluspath.GraphicsPath.GetPathData
title: GraphicsPath::GetPathData (gdipluspath.h)
description: The GraphicsPath::GetPathData method gets an array of points and an array of point types from this path. Together, these two arrays define the lines, curves, figures, and markers of this path.
helpviewer_keywords: ["GetPathData","GetPathData method [GDI+]","GetPathData method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","GetPathData method","GraphicsPath.GetPathData","GraphicsPath::GetPathData","_gdiplus_CLASS_GraphicsPath_GetPathData_pathData_","gdiplus._gdiplus_CLASS_GraphicsPath_GetPathData_pathData_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPathData_pathData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getpathdata.htm
ms.date: 12/05/2018
ms.keywords: GetPathData, GetPathData method [GDI+], GetPathData method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPathData method, GraphicsPath.GetPathData, GraphicsPath::GetPathData, _gdiplus_CLASS_GraphicsPath_GetPathData_pathData_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPathData_pathData_
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
 - GraphicsPath::GetPathData
 - gdipluspath/GraphicsPath::GetPathData
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
 - GraphicsPath.GetPathData
---

# GraphicsPath::GetPathData


## -description

The <b>GraphicsPath::GetPathData</b> method gets an array of points and an array of point types from this path. Together, these two arrays define the lines, curves, figures, and markers of this path.

## -parameters

### -param pathData [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a> object that receives the path data. The <i>Points</i> data member of the <b>PathData</b> object receives a pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> objects that contains the path points. The <i>Types</i> data member of the <b>PathData</b> object receives a pointer to an array of bytes that contains the point types. The <i>Count</i> data member of the <b>PathData</b> object receives an integer that indicates the number of elements in the <i>Points</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.

You do not have to allocate or deallocate memory for the array of points or the array of types. The <b>GraphicsPath::GetPathData</b> method allocates memory for the arrays (points and types) that it returns. The <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a> destructor deallocates the memory for those arrays.


#### Examples



The following example creates and draws a path that has a line, a rectangle, an ellipse, and a curve. The code gets the path's points and types by passing the address of a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a> object to the <b>GraphicsPath::GetPathData</b> method. Then the code draws each of the path's data points.


```cpp
VOID GetPathDataExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has a line, a rectangle, an ellipse, and a curve.
   GraphicsPath path;
   
   PointF points[] = {
      PointF(200, 200),
      PointF(250, 240),
      PointF(200, 300),
      PointF(300, 310),
      PointF(250, 350)};

   path.AddLine(20, 100, 150, 200);
   path.AddRectangle(Rect(40, 30, 80, 60));
   path.AddEllipse(Rect(200, 30, 200, 100));
   path.AddCurve(points, 5);

   // Draw the path.
   Pen pen(Color(255, 0, 0, 255));
   graphics.DrawPath(&pen, &path);

   // Get the path data.
   PathData pathData;
   path.GetPathData(&pathData);

   // Draw the path's data points.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j < pathData.Count; ++j)
   {
      graphics.FillEllipse(
         &brush, 
         pathData.Points[j].X - 3.0f, 
         pathData.Points[j].Y - 3.0f,
         6.0f,
         6.0f);
   }
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)">GetPathPoints Methods</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GraphicsPath::GetPathTypes</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>
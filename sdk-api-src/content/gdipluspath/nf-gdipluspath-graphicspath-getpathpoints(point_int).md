---
UID: NF:gdipluspath.GraphicsPath.GetPathPoints(Point,INT)
title: GraphicsPath::GetPathPoints(OUT Point,IN INT) (gdipluspath.h)
description: The GraphicsPath::GetPathPoints method gets this path's array of points. The array contains the endpoints and control points of the lines and Bézier splines that are used to draw the path.
helpviewer_keywords: ["GetPathPoints","GetPathPoints method [GDI+]","GetPathPoints method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","GetPathPoints method","GraphicsPath.GetPathPoints","GraphicsPath.GetPathPoints(OUT Point","IN INT)","GraphicsPath.GetPathPoints(Point*","INT)","GraphicsPath::GetPathPoints","GraphicsPath::GetPathPoints(OUT Point","IN INT)","_gdiplus_CLASS_GraphicsPath_GetPathPoints_Point_points_INT_count_","gdiplus._gdiplus_CLASS_GraphicsPath_GetPathPoints_Point_points_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPathPoints_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathgetpathpointsmethods\getpathpoints.htm
ms.date: 12/05/2018
ms.keywords: GetPathPoints, GetPathPoints method [GDI+], GetPathPoints method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPathPoints method, GraphicsPath.GetPathPoints, GraphicsPath.GetPathPoints(OUT Point,IN INT), GraphicsPath.GetPathPoints(Point*,INT), GraphicsPath::GetPathPoints, GraphicsPath::GetPathPoints(OUT Point,IN INT), _gdiplus_CLASS_GraphicsPath_GetPathPoints_Point_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPathPoints_Point_points_INT_count_
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
 - GraphicsPath::GetPathPoints
 - gdipluspath/GraphicsPath::GetPathPoints
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
 - GraphicsPath.GetPathPoints
---

# GraphicsPath::GetPathPoints(OUT Point,IN INT)


## -description

The <b>GraphicsPath::GetPathPoints</b> method gets this path's array of points. The array contains the endpoints and control points of the lines and Bézier splines that are used to draw the path.

## -parameters

### -param points [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects that receives the data points. You must allocate memory for this array. You can call the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a> method to determine the required size of the array. The size, in bytes, should be the return value of <b>GraphicsPath::GetPointCount</b> multiplied by <b>sizeof</b>(<b>Point</b>).

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. Set this parameter equal to the return value of the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a> method.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.


#### Examples



The following example creates and draws a path that has a line, a rectangle, an ellipse, and a curve. The code calls the path's <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a> method to determine the number of data points that are stored in the path. The code allocates a buffer large enough to receive the array of data points and passes the address of that buffer to the <b>GraphicsPath::GetPathPoints</b> method. Finally, the code draws each of the path's data points.


```cpp
VOID GetPathPointsExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has a line, a rectangle, an ellipse, and a curve.
   GraphicsPath path;

   Point points[] = {
      Point(200, 200),
      Point(250, 240),
      Point(200, 300),
      Point(300, 310),
      Point(250, 350)};

   path.AddLine(20, 100, 150, 200);
   path.AddRectangle(Rect(40, 30, 80, 60));
   path.AddEllipse(Rect(200, 30, 200, 100));
   path.AddCurve(points, 5);

   // Draw the path.
   Pen pen(Color(255, 0, 0, 255));
   graphics.DrawPath(&pen, &path);

   // Get the path points.
   INT count = path.GetPointCount();
   Point* dataPoints = new Point[count];
   path.GetPathPoints(dataPoints, count);

   // Draw the path's data points.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j < count; ++j)
   {
      graphics.FillEllipse(
         &brush, 
         dataPoints[j].X - 3.0f, 
         dataPoints[j].Y - 3.0f,
         6.0f,
         6.0f);
   }
   delete [] dataPoints; 
}
Color(255, 255, 0,  0)
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GraphicsPath::GetPathData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GraphicsPath::GetPathTypes</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
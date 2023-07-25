---
UID: NF:gdipluspath.GraphicsPath.GetPathPoints(PointF,INT)
title: GraphicsPath::GetPathPoints
description: The GraphicsPath::GetPathPoints method gets this path's array of points.
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::GetPathPoints"]
ms.assetid: b8477156-4557-4aa7-900e-61eb9108ec38
ms.date: 05/13/2019
ms.keywords: GraphicsPath::GetPathPoints
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdipluspath.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - GraphicsPath::GetPathPoints
 - gdipluspath/GraphicsPath::GetPathPoints
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::GetPathPoints
---

# GraphicsPath::GetPathPoints


## -description

The **GraphicsPath::GetPathPoints** method gets this path's array of points.
The array contains the endpoints and control points of the lines and Bézier splines that are used to draw the path.

## -parameters

### -param points

Pointer to an array of **PointF** objects that receives the data points.
You must allocate memory for this array.
You can call the **GraphicsPath::GetPointCount** method to determine the required size of the array.
The size, in bytes, should be the return value of **GraphicsPath::GetPointCount** multiplied by `sizeof(PointF)`.

### -param count

Integer that specifies the number of elements in the points array.
Set this parameter equal to the return value of the **GraphicsPath::GetPointCount** method.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has an array of points and an array of types.
Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points.
Possible point types and flags are listed in the PathPointType enumeration.

#### Examples

The following example creates and draws a path that has a line, a rectangle, an ellipse, and a curve.
The code calls the path's **GraphicsPath::GetPointCount** method to determine the number of data points that are stored in the path.
The code allocates a buffer large enough to receive the array of data points and passes the address of that buffer to the **GraphicsPath::GetPathPoints** method.
Finally, the code draws each of the path's data points.

```cpp
VOID GetPathPointsExample(HDC hdc)
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

   // Get the path points.
   INT count = path.GetPointCount();
   PointF* dataPoints = new PointF[count];  
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

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GraphicsPath::GetPathData</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GraphicsPath::GetPathTypes</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a>

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

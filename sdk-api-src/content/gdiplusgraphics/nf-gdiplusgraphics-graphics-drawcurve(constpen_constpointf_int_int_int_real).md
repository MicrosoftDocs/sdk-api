---
UID: NF:gdiplusgraphics.Graphics.DrawCurve(constPen,constPointF,INT,INT,INT,REAL)
title: Graphics::DrawCurve(IN const Pen,IN const PointF,IN INT,IN INT,IN INT,IN REAL) (gdiplusgraphics.h)
description: The Graphics::DrawCurve method draws a cardinal spline. (overload 6/6)
helpviewer_keywords: ["DrawCurve","DrawCurve method [GDI+]","DrawCurve method [GDI+]","Graphics class","Graphics class [GDI+]","DrawCurve method","Graphics.DrawCurve","Graphics.DrawCurve(IN const Pen","IN const PointF","IN INT","IN INT","IN INT","IN REAL)","Graphics.DrawCurve(const Pen*","const PointF*","INT","INT","INT","REAL)","Graphics::DrawCurve","Graphics::DrawCurve(IN const Pen","IN const PointF","IN INT","IN INT","IN INT","IN REAL)","_gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_PointF_points_INT_count_INT_offset_INT_numberOfSegments_RE","gdiplus._gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_PointF_points_INT_count_INT_offset_INT_numberOfSegments_RE"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_PointF_points_INT_count_INT_offset_INT_numberOfSegments_RE.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawcurvemethods\drawcurve_65penpen_pointfpoints_intcount_intoffset.htm
ms.date: 12/05/2018
ms.keywords: DrawCurve, DrawCurve method [GDI+], DrawCurve method [GDI+],Graphics class, Graphics class [GDI+],DrawCurve method, Graphics.DrawCurve, Graphics.DrawCurve(IN const Pen,IN const PointF,IN INT,IN INT,IN INT,IN REAL), Graphics.DrawCurve(const Pen*,const PointF*,INT,INT,INT,REAL), Graphics::DrawCurve, Graphics::DrawCurve(IN const Pen,IN const PointF,IN INT,IN INT,IN INT,IN REAL), _gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_PointF_points_INT_count_INT_offset_INT_numberOfSegments_RE, gdiplus._gdiplus_CLASS_Graphics_DrawCurve_Pen_pen_PointF_points_INT_count_INT_offset_INT_numberOfSegments_RE
req.header: gdiplusgraphics.h
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
 - Graphics::DrawCurve
 - gdiplusgraphics/Graphics::DrawCurve
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
 - Graphics.DrawCurve
---

# Graphics::DrawCurve(IN const Pen,IN const PointF,IN INT,IN INT,IN INT,IN REAL)


## -description

The <b>Graphics::DrawCurve</b> method draws a cardinal spline.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the cardinal spline.

### -param points [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

Pointer to an array of 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> objects that specify the coordinates that the cardinal spline passes through.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array.

### -param offset [in]

Type: <b>INT</b>

Integer that specifies the element in the 
					<i>points</i> array that specifies the point at which the cardinal spline begins.

### -param numberOfSegments [in]

Type: <b>INT</b>

Integer that specifies the number of segments in the cardinal spline.

### -param tension [in]

Type: <b>REAL</b>

Real number that specifies how tightly the curve bends through the coordinates of the cardinal spline.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A segment is defined as a curve that connects two consecutive points in the cardinal spline. The ending point of each segment is the starting point for the next. The 
				<i>numberOfSegments</i> parameter must not be greater than the 
				<i>count</i> parameter minus the 
				<i>offset</i> parameter plus one.


#### Examples



The following example draws a cardinal spline.


```cpp
VOID Example_DrawCurve5(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a Pen object and an array of PointF objects.
   Pen greenPen(Color::Green, 3);
   PointF point1(100.0f, 100.0f);
   PointF point2(200.0f, 50.0f);
   PointF point3(400.0f, 10.0f);
   PointF point4(500.0f, 100.0f);

   PointF curvePoints[4] = {
   point1,
   point2,
   point3,
   point4};

   PointF* pcurvePoints = curvePoints;

   // Specify offset, number of segments to draw, and tension.
   int offset = 1;
   int segments = 2;
   REAL tension = 1.0f;

   // Draw the curve.
   graphics.DrawCurve(&greenPen, curvePoints, 4, offset, segments, tension);

   //Draw the points in the curve.
   SolidBrush redBrush(Color::Red);
   graphics.FillEllipse(&redBrush, Rect(95, 95, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(195, 45, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(395, 5, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(495, 95, 10, 10));
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-cardinal-splines-about">Cardinal Splines</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpointf_inint_inreal)">DrawClosedCurve Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-cardinal-splines-use">Drawing Cardinal Splines</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>

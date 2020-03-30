---
UID: NF:gdiplusgraphics.Graphics.DrawClosedCurve(IN const Pen,IN const Point,IN INT)
title: Graphics::DrawClosedCurve(IN const Pen,IN const Point,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawClosedCurve method draws a closed cardinal spline.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawclosedcurvemethods\drawclosedcurve.htm
ms.date: 12/05/2018
ms.keywords: DrawClosedCurve, DrawClosedCurve method [GDI+], DrawClosedCurve method [GDI+],Graphics class, Graphics class [GDI+],DrawClosedCurve method, Graphics.DrawClosedCurve, Graphics.DrawClosedCurve(IN const Pen,IN const Point,IN INT), Graphics.DrawClosedCurve(const Pen*,const Point*,INT), Graphics::DrawClosedCurve, Graphics::DrawClosedCurve(IN const Pen,IN const Point,IN INT), _gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_Point_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_Point_points_INT_count_
f1_keywords:
- gdiplusgraphics/Graphics.DrawClosedCurve
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- Graphics.DrawClosedCurve
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::DrawClosedCurve(IN const Pen,IN const Point,IN INT)


## -description


The <b>Graphics::DrawClosedCurve</b> method draws a closed cardinal spline.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the closed cardinal spline. 


### -param points [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects that specify the coordinates of the closed cardinal spline. The array of <b>Point</b> objects must contain a minimum of three elements. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



In a closed cardinal spline, the curve continues through the last point in the 
				<i>points</i> array and connects with the first point in the array.


#### Examples



The following example draws a closed cardinal spline.


```cpp

VOID Example_DrawClosedCurve(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a Pen object and an array of Point objects.
   Pen greenPen(Color(255, 0, 0, 255), 3);

   Point point1(100, 100);
   Point point2(200, 50);
   Point point3(400, 10);
   Point point4(500, 100);
   Point point5(600, 200);
   Point point6(700, 400);
   Point point7(500, 500);

   Point curvePoints[7] = {
      point1,
      point2,
      point3,
      point4,
      point5,
      point6,
      point7};

   // Draw the closed curve.
   graphics.DrawClosedCurve(&greenPen, curvePoints, 7);

   // Draw the points in the curve.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   graphics.FillEllipse(&redBrush, Rect(95, 95, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(495, 95, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(495, 495, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(195, 45, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(395, 5, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(595, 195, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(695, 395, 10, 10));
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-cardinal-splines-about">Cardinal Splines</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inint_inint_inreal)">DrawCurve Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-drawing-cardinal-splines-use">Drawing Cardinal Splines</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpointf_inint_infillmode_inreal)">FillClosedCurve Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
 

 


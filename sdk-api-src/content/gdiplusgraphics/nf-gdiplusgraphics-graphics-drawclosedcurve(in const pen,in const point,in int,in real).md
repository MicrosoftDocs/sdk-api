---
UID: NF:gdiplusgraphics.Graphics.DrawClosedCurve(IN const Pen,IN const Point,IN INT,IN REAL)
title: Graphics::DrawClosedCurve(IN const Pen,IN const Point,IN INT,IN REAL)
author: windows-sdk-content
description: The Graphics::DrawClosedCurve method draws a closed cardinal spline.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_Point_points_INT_count_REAL_tension_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawclosedcurvemethods\drawclosedcurve_94penpen_pointpoints_intcount_realtensio.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawClosedCurve, DrawClosedCurve method [GDI+], DrawClosedCurve method [GDI+],Graphics class, Graphics class [GDI+],DrawClosedCurve method, Graphics.DrawClosedCurve, Graphics.DrawClosedCurve(IN const Pen,IN const Point,IN INT,IN REAL), Graphics.DrawClosedCurve(const Pen*,const Point*,INT,REAL), Graphics::DrawClosedCurve, Graphics::DrawClosedCurve(IN const Pen,IN const Point,IN INT,IN REAL), _gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_Point_points_INT_count_REAL_tension_, gdiplus._gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_Point_points_INT_count_REAL_tension_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusgraphics.h
: 
- Graphics.DrawClosedCurve
: 
req.product: GDI+ 1.0
---

# Graphics::DrawClosedCurve(IN const Pen,IN const Point,IN INT,IN REAL)


## -description


The <b>Graphics::DrawClosedCurve</b> method draws a closed cardinal spline.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a pen that is used to draw the closed cardinal spline. 


### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> objects that specify the coordinates of the closed cardinal spline. The array of <b>Point</b> objects must contain a minimum of three elements. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. 


### -param tension [in]

Type: <b>REAL</b>

Real number that specifies how tightly the curve bends through the coordinates of the closed cardinal spline. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Each ending point is the starting point for the next cardinal spline. In a closed cardinal spline, the curve continues through the last point in the 
				<i>points</i> array and connects with the first point in the array.


#### Examples



The following example draws a closed cardinal spline.


```cpp

VOID Example_DrawClosedCurve2(HDC hdc)
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
   graphics.DrawClosedCurve(&greenPen, curvePoints, 7, 1.0);

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




<a href="https://msdn.microsoft.com/4fc62f00-7006-4ade-bfcc-091a3a97d889">Cardinal Splines</a>



<a href="https://msdn.microsoft.com/3b29e150-26ac-46c6-8aa5-984aeb03392a">DrawCurve Methods</a>



<a href="https://msdn.microsoft.com/0bb84f55-18d0-4a4c-bc5b-7803aa807954">Drawing Cardinal Splines</a>



<a href="https://msdn.microsoft.com/378f0d34-7328-45e5-9f55-826bdaed3aab">FillClosedCurve Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>
 

 


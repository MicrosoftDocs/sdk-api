---
UID: NF:gdiplusgraphics.Graphics.DrawClosedCurve(IN const Pen,IN const PointF,IN INT,IN REAL)
title: Graphics::DrawClosedCurve(IN const Pen,IN const PointF,IN INT,IN REAL)
author: windows-sdk-content
description: The Graphics::DrawClosedCurve method draws a closed cardinal spline.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_PointF_points_INT_count_REAL_tension_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawclosedcurvemethods\drawclosedcurve_28penpen_pointfpoints_intcount_realtensi.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawClosedCurve, DrawClosedCurve method [GDI+], DrawClosedCurve method [GDI+],Graphics class, Graphics class [GDI+],DrawClosedCurve method, Graphics.DrawClosedCurve, Graphics.DrawClosedCurve(IN const Pen,IN const PointF,IN INT,IN REAL), Graphics.DrawClosedCurve(const Pen*,const PointF*,INT,REAL), Graphics::DrawClosedCurve, Graphics::DrawClosedCurve(IN const Pen,IN const PointF,IN INT,IN REAL), _gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_PointF_points_INT_count_REAL_tension_, gdiplus._gdiplus_CLASS_Graphics_DrawClosedCurve_Pen_pen_PointF_points_INT_count_REAL_tension_
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
req.product: GDI+ 1.0
---

# Graphics::DrawClosedCurve(IN const Pen,IN const PointF,IN INT,IN REAL)


## -description


The <b>Graphics::DrawClosedCurve</b> method draws a closed cardinal spline.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>*</b>

Pointer to a pen that is used to draw the closed cardinal spline. 


### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects that specify the coordinates of the closed cardinal spline. The array of <b>PointF</b> objects must contain a minimum of three elements. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. 


### -param tension [in]

Type: <b>REAL</b>

Real number that specifies how tightly the curve bends through the coordinates of the closed cardinal spline. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



Each ending point is the starting point for the next cardinal spline. In a closed cardinal spline, the curve continues through the last point in the 
				<i>points</i> array and connects with the first point in the array.


#### Examples



The following example draws a closed cardinal spline.


```cpp

VOID Example_DrawClosedCurve4(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a Pen object and an array of PointF objects.
   Pen greenPen(Color(255, 0, 0, 255), 3);
   PointF point1(100.0f, 100.0f);
   PointF point2(200.0f, 50.0f);
   PointF point3(400.0f, 10.0f);
   PointF point4(500.0f, 100.0f);
   PointF point5(600.0f, 200.0f);
   PointF point6(700.0f, 400.0f);
   PointF point7(500.0f, 500.0f);

   PointF curvePoints[7] = {
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




<a href="https://msdn.microsoft.com/en-us/library/ms536358(v=VS.85).aspx">Cardinal Splines</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535742(v=VS.85).aspx">DrawCurve Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533934(v=VS.85).aspx">Drawing Cardinal Splines</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535765(v=VS.85).aspx">FillClosedCurve Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
 

 


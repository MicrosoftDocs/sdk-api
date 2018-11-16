---
UID: NF:gdiplusgraphics.Graphics.DrawBeziers(IN const Pen,IN const PointF,IN INT)
title: Graphics::DrawBeziers(IN const Pen,IN const PointF,IN INT)
author: windows-sdk-content
description: The Graphics::DrawBeziers method draws a sequence of connected B&#233;zier splines.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawBeziers_Pen_pen_PointF_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawbeziersmethods\drawbeziers_29penpen_pointfpoints_intcount.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DrawBeziers, DrawBeziers method [GDI+], DrawBeziers method [GDI+],Graphics class, Graphics class [GDI+],DrawBeziers method, Graphics.DrawBeziers, Graphics.DrawBeziers(IN const Pen,IN const PointF,IN INT), Graphics.DrawBeziers(const Pen*,const PointF*,INT), Graphics::DrawBeziers, Graphics::DrawBeziers(IN const Pen,IN const PointF,IN INT), _gdiplus_CLASS_Graphics_DrawBeziers_Pen_pen_PointF_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawBeziers_Pen_pen_PointF_points_INT_count_
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
 - Graphics.DrawBeziers
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
- Graphics.DrawBeziers
: 
req.product: GDI+ 1.0
---

# Graphics::DrawBeziers(IN const Pen,IN const PointF,IN INT)


## -description


The <b>Graphics::DrawBeziers</b> method draws a sequence of connected Bézier splines.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a pen that is used to draw the Bézier splines. 


### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> objects that specify the starting, ending, and control points of the Bézier splines. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A Bézier spline does not pass through its control points. The control points act as magnets, pulling the curve in certain directions to influence the way a Bézier spline bends. Each Bézier spline requires a starting point and an ending point. Each ending point is the starting point for the next Bézier spline. 


#### Examples



The following example draws a pair of Bézier curves.


```cpp

VOID Example_DrawBeziers2(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a Pen object and an array of PointF objects.
   Pen greenPen(Color(255, 0, 255, 0), 3);

   PointF startPoint(100.0f, 100.0f);
   PointF ctrlPoint1(200.0f, 50.0f);
   PointF ctrlPoint2(400.0f, 10.0f);
   PointF endPoint1(500.0f, 100.0f);
   PointF ctrlPoint3(600.0f, 200.0f);
   PointF ctrlPoint4(700.0f, 400.0f);
   PointF endPoint2(500.0f, 500.0f);

   PointF curvePoints[7] = {
      startPoint,
      ctrlPoint1,
      ctrlPoint2,
      endPoint1,
      ctrlPoint3,
      ctrlPoint4,
      endPoint2};

   // Draw the Bezier curves.
   graphics.DrawBeziers(&greenPen, curvePoints, 7);

   // Draw the control and end points.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   graphics.FillEllipse(&redBrush, Rect(100 - 5, 100 - 5, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(500 - 5, 100 - 5, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(500 - 5, 500 - 5, 10, 10));
   SolidBrush blueBrush(Color(255, 0, 0, 255));
   graphics.FillEllipse(&blueBrush, Rect(200 - 5, 50 - 5, 10, 10));
   graphics.FillEllipse(&blueBrush, Rect(400 - 5, 10 - 5, 10, 10));
   graphics.FillEllipse(&blueBrush, Rect(600 - 5, 200 - 5, 10, 10));
   graphics.FillEllipse(&blueBrush, Rect(700 - 5, 400 - 5, 10, 10));
}
```





## -see-also




<a href="https://msdn.microsoft.com/3ee279ea-20cc-4089-b1a5-13bf1c7c4942">Bézier Splines</a>



<a href="https://msdn.microsoft.com/96060c2f-85cc-449f-bdc6-f4bab887d11f">DrawBezier Methods</a>



<a href="https://msdn.microsoft.com/af91f612-7e65-4a36-8449-32410d275b00">DrawBeziers</a>



<a href="https://msdn.microsoft.com/af19e82b-0d13-4fb0-981e-8d5dd1bbfb36">Drawing Bézier Splines</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>
 

 


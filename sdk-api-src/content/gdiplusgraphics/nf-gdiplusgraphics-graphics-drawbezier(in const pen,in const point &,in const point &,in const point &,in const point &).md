---
UID: NF:gdiplusgraphics.Graphics.DrawBezier(IN const Pen,IN const Point &,IN const Point &,IN const Point &,IN const Point &)
title: Graphics::DrawBezier(IN const Pen,IN const Point &,IN const Point &,IN const Point &,IN const Point &)
author: windows-sdk-content
description: The Graphics::DrawBezier method draws a B&#233;zier spline.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_Point_pt1_Point_pt2_Point_pt3_Point_pt4_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawbeziermethods\drawbezier.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DrawBezier, DrawBezier method [GDI+], DrawBezier method [GDI+],Graphics class, Graphics class [GDI+],DrawBezier method, Graphics.DrawBezier, Graphics.DrawBezier(IN const Pen,IN const Point &,IN const Point &,IN const Point &,IN const Point &), Graphics.DrawBezier(const Pen*,const POINT&,const POINT&,const POINT&,const POINT&), Graphics::DrawBezier, Graphics::DrawBezier(IN const Pen,IN const Point &,IN const Point &,IN const Point &,IN const Point &), _gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_Point_pt1_Point_pt2_Point_pt3_Point_pt4_, gdiplus._gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_Point_pt1_Point_pt2_Point_pt3_Point_pt4_
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
 - Graphics.DrawBezier
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
- Graphics.DrawBezier
: 
req.product: GDI+ 1.0
---

# Graphics::DrawBezier(IN const Pen,IN const Point &,IN const Point &,IN const Point &,IN const Point &)


## -description


The <b>Graphics::DrawBezier</b> method draws a Bézier spline.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a pen that is used to draw the Bézier spline. 


### -param pt1 [in, ref]

Type: <b>const POINT</b>

Reference to the starting point of the Bézier spline. 


### -param pt2 [in, ref]

Type: <b>const POINT</b>

Reference to the first control point of the Bézier spline. 


### -param pt3 [in, ref]

Type: <b>const POINT</b>

Reference to the second control point of the Bézier spline. 


### -param pt4 [in, ref]

Type: <b>const POINT</b>

Reference to the ending point of the Bézier spline. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A Bézier spline does not pass through its control points. The control points act as magnets, pulling the curve in certain directions to influence the way the Bézier spline bends.


#### Examples



The following example draws a Bézier curve.


```cpp

VOID Example_DrawBezier(HDC hdc)
{
   Graphics graphics(hdc);

   // Set up the pen and curve points.
   Pen greenPen(Color(255, 0, 255, 0));
   Point startPoint(100, 100);
   Point controlPoint1(200, 10);
   Point controlPoint2(350, 50);
   Point endPoint(500, 100);

   //Draw the curve.
   graphics.DrawBezier(&greenPen, startPoint, controlPoint1, controlPoint2, endPoint);

   //Draw the end points and control points.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   SolidBrush blueBrush(Color(255, 0, 0, 255));
   graphics.FillEllipse(&redBrush, 100 - 5, 100 - 5, 10, 10);
   graphics.FillEllipse(&redBrush, 500 - 5, 100 - 5, 10, 10);
   graphics.FillEllipse(&blueBrush, 200 - 5, 10 - 5, 10, 10);
   graphics.FillEllipse(&blueBrush, 350 - 5, 50 - 5, 10, 10);
}
```





## -see-also




<a href="https://msdn.microsoft.com/3ee279ea-20cc-4089-b1a5-13bf1c7c4942">Bézier Splines</a>



<a href="https://msdn.microsoft.com/96060c2f-85cc-449f-bdc6-f4bab887d11f">DrawBezier</a>



<a href="https://msdn.microsoft.com/af91f612-7e65-4a36-8449-32410d275b00">DrawBeziers Methods</a>



<a href="https://msdn.microsoft.com/af19e82b-0d13-4fb0-981e-8d5dd1bbfb36">Drawing Bézier Splines</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>
 

 


---
UID: NF:gdiplusgraphics.Graphics.DrawBezier(constPen,constPointF&,constPointF&,constPointF&,constPointF&)
title: Graphics::DrawBezier(IN const Pen,IN const PointF &,IN const PointF &,IN const PointF &,IN const PointF &) (gdiplusgraphics.h)
description: The Graphics::DrawBezier method draws a Bézier spline. (overload 3/3)
helpviewer_keywords: ["DrawBezier","DrawBezier method [GDI+]","DrawBezier method [GDI+]","Graphics class","Graphics class [GDI+]","DrawBezier method","Graphics.DrawBezier","Graphics.DrawBezier(IN const Pen","IN const PointF &","IN const PointF &","IN const PointF &","IN const PointF &)","Graphics.DrawBezier(const Pen*","const POINTF&","const POINTF&","const POINTF&","const POINTF&)","Graphics::DrawBezier","Graphics::DrawBezier(IN const Pen","IN const PointF &","IN const PointF &","IN const PointF &","IN const PointF &)","_gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_PointF_pt1_PointF_pt2_PointF_pt3_PointF_pt4_","gdiplus._gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_PointF_pt1_PointF_pt2_PointF_pt3_PointF_pt4_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_PointF_pt1_PointF_pt2_PointF_pt3_PointF_pt4_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawbeziermethods\drawbezier_36penpen_pointfamppt1_pointfamppt2_point.htm
ms.date: 12/05/2018
ms.keywords: DrawBezier, DrawBezier method [GDI+], DrawBezier method [GDI+],Graphics class, Graphics class [GDI+],DrawBezier method, Graphics.DrawBezier, Graphics.DrawBezier(IN const Pen,IN const PointF &,IN const PointF &,IN const PointF &,IN const PointF &), Graphics.DrawBezier(const Pen*,const POINTF&,const POINTF&,const POINTF&,const POINTF&), Graphics::DrawBezier, Graphics::DrawBezier(IN const Pen,IN const PointF &,IN const PointF &,IN const PointF &,IN const PointF &), _gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_PointF_pt1_PointF_pt2_PointF_pt3_PointF_pt4_, gdiplus._gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_PointF_pt1_PointF_pt2_PointF_pt3_PointF_pt4_
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
 - Graphics::DrawBezier
 - gdiplusgraphics/Graphics::DrawBezier
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
 - Graphics.DrawBezier
---

# Graphics::DrawBezier(IN const Pen,IN const PointF &,IN const PointF &,IN const PointF &,IN const PointF &)


## -description

The <b>Graphics::DrawBezier</b> method draws a Bézier spline.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the Bézier spline.

### -param pt1 [in, ref]

Type: <b>const POINTF</b>

Reference to the starting point of the Bézier spline.

### -param pt2 [in, ref]

Type: <b>const POINTF</b>

Reference to the first control point of the Bézier spline.

### -param pt3 [in, ref]

Type: <b>const POINTF</b>

Reference to the second control point of the Bézier spline.

### -param pt4 [in, ref]

Type: <b>const POINTF</b>

Reference to the ending point of the Bézier spline.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A Bézier spline does not pass through its control points. The control points act as magnets, pulling the curve in certain directions to influence the way the Bézier spline bends.


#### Examples



The following example draws a Bézier curve.


```cpp

VOID Example_DrawBezier2(HDC hdc)
{
   Graphics graphics(hdc);

   // Set up the pen and curve points.
   Pen greenPen(Color(255, 0, 255, 0));
   PointF startPoint(100.0f, 100.0f);
   PointF controlPoint1(200.0f, 10.0f);
   PointF controlPoint2(350.0f, 50.0f);
   PointF endPoint(500.0f, 100.0f);

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

<a href="/windows/desktop/gdiplus/-gdiplus-bezier-splines-about">Bézier Splines</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_)">DrawBezier</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)">DrawBeziers Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-bezier-splines-use">Drawing Bézier Splines</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

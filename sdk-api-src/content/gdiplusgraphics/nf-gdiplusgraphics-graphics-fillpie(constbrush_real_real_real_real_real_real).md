---
UID: NF:gdiplusgraphics.Graphics.FillPie(constBrush,REAL,REAL,REAL,REAL,REAL,REAL)
title: Graphics::FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL) (gdiplusgraphics.h)
description: The Graphics::FillPie method uses a brush to fill the interior of a pie. (overload 1/4)
helpviewer_keywords: ["FillPie","FillPie method [GDI+]","FillPie method [GDI+]","Graphics class","Graphics class [GDI+]","FillPie method","Graphics.FillPie","Graphics.FillPie(IN const Brush","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL)","Graphics.FillPie(const Brush*","REAL","REAL","REAL","REAL","REAL","REAL)","Graphics::FillPie","Graphics::FillPie(IN const Brush","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL)","_gdiplus_CLASS_Graphics_FillPie_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REA","gdiplus._gdiplus_CLASS_Graphics_FillPie_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REA"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillPie_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REA.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillpiemethods\fillpie_76brushbrush_realx_realy_realwidth_realh.htm
ms.date: 12/05/2018
ms.keywords: FillPie, FillPie method [GDI+], FillPie method [GDI+],Graphics class, Graphics class [GDI+],FillPie method, Graphics.FillPie, Graphics.FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), Graphics.FillPie(const Brush*,REAL,REAL,REAL,REAL,REAL,REAL), Graphics::FillPie, Graphics::FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_FillPie_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REA, gdiplus._gdiplus_CLASS_Graphics_FillPie_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REA
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
 - Graphics::FillPie
 - gdiplusgraphics/Graphics::FillPie
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
 - Graphics.FillPie
---

# Graphics::FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description

The <b>Graphics::FillPie</b> method uses a brush to fill the interior of a pie.

## -parameters

### -param brush [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to paint the interior of the pie.

### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle that bounds the ellipse. A curved portion of the ellipse is the arc of the pie.

### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle that bounds the ellipse.

### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle that bounds the ellipse.

### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle that bounds the ellipse.

### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the x-axis and the starting point of the pie's arc.

### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the starting and ending points of the pie's arc.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A pie is a portion of the interior of an ellipse (it is bounded by an elliptical curve and two radial lines). The 
				<i>startAngle</i> and <i>sweepAngle</i> specify the portion of the ellipse to be used.


#### Examples



The following example defines a pie and then fills it.


```cpp
VOID Example_FillPie4(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Define the pie shape.
   REAL x = 0.0f;
   REAL y = 2.0f;
   REAL width = 200.8f;
   REAL height = 100.1f;
   REAL startAngle = 0.0f;
   REAL sweepAngle = 45.7f;

   // Fill the pie.
   graphics.FillPie(&blackBrush, x, y, width, height, startAngle, sweepAngle);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

---
UID: NF:gdiplusgraphics.Graphics.FillClosedCurve(constBrush,constPoint,INT,FillMode,REAL)
title: Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT,IN FillMode,IN REAL) (gdiplusgraphics.h)
description: The Graphics::FillClosedCurve method creates a closed cardinal spline from an array of points and uses a brush to fill, according to a specified mode, the interior of the spline. (overload 2/2)
helpviewer_keywords: ["FillClosedCurve","FillClosedCurve method [GDI+]","FillClosedCurve method [GDI+]","Graphics class","Graphics class [GDI+]","FillClosedCurve method","Graphics.FillClosedCurve","Graphics.FillClosedCurve(IN const Brush","IN const Point","IN INT","IN FillMode","IN REAL)","Graphics.FillClosedCurve(const Brush*","const Point*","INT","FillMode","REAL)","Graphics::FillClosedCurve","Graphics::FillClosedCurve(IN const Brush","IN const Point","IN INT","IN FillMode","IN REAL)","_gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_FillMode_fillMode_REAL_te","gdiplus._gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_FillMode_fillMode_REAL_te"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_FillMode_fillMode_REAL_te.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillclosedcurvemethods\fillclosedcurve_20brushbrush_pointpoints_intcount_fillmo.htm
ms.date: 12/05/2018
ms.keywords: FillClosedCurve, FillClosedCurve method [GDI+], FillClosedCurve method [GDI+],Graphics class, Graphics class [GDI+],FillClosedCurve method, Graphics.FillClosedCurve, Graphics.FillClosedCurve(IN const Brush,IN const Point,IN INT,IN FillMode,IN REAL), Graphics.FillClosedCurve(const Brush*,const Point*,INT,FillMode,REAL), Graphics::FillClosedCurve, Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT,IN FillMode,IN REAL), _gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_FillMode_fillMode_REAL_te, gdiplus._gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_FillMode_fillMode_REAL_te
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
 - Graphics::FillClosedCurve
 - gdiplusgraphics/Graphics::FillClosedCurve
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
 - Graphics.FillClosedCurve
---

# Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT,IN FillMode,IN REAL)


## -description

The <b>Graphics::FillClosedCurve</b> method creates a closed cardinal spline from an array of points and uses a brush to fill, according to a specified mode, the interior of the spline.

## -parameters

### -param brush [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to paint the interior of the spline.

### -param points [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of points that this method uses to create a closed cardinal spline. Each point in the array is a point on the spline.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the 
					<i>points</i> array.

### -param fillMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a> enumeration that specifies how to fill a closed area that is created when the curve passes over itself.

### -param tension [in]

Type: <b>REAL</b>

Optional. Nonnegative real number that specifies how tightly the spline bends as it passes through the points. A value of 0 specifies that the spline is a sequence of straight lines. As the value increases, the curve becomes fuller. The default value is 0.5f.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-cardinal-splines-about">Cardinal Splines</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-cardinal-splines-use">Drawing Cardinal Splines</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-open-and-closed-curves-about">Open and Closed Curves</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>

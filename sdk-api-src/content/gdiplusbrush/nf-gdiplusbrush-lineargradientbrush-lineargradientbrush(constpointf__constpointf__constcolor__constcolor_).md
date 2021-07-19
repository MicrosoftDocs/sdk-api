---
UID: NF:gdiplusbrush.LinearGradientBrush.LinearGradientBrush(constPointF&,constPointF&,constColor&,constColor&)
title: LinearGradientBrush::LinearGradientBrush(IN const PointF &,IN const PointF &,IN const Color &,IN const Color &) (gdiplusbrush.h)
description: Creates a LinearGradientBrush::LinearGradientBrush object from a set of boundary points and boundary colors.
helpviewer_keywords: ["LinearGradientBrush","LinearGradientBrush class [GDI+]","LinearGradientBrush constructor","LinearGradientBrush constructor [GDI+]","LinearGradientBrush constructor [GDI+]","LinearGradientBrush class","LinearGradientBrush.LinearGradientBrush","LinearGradientBrush.LinearGradientBrush(IN const PointF &","IN const PointF &","IN const Color &","IN const Color &)","LinearGradientBrush.LinearGradientBrush(const PointF&","const PointF&","const Color&","const Color&)","LinearGradientBrush::LinearGradientBrush","LinearGradientBrush::LinearGradientBrush(IN const PointF &","IN const PointF &","IN const Color &","IN const Color &)","_gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_PointF_point1_PointF_point2_Color_color1_Colo","gdiplus._gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_PointF_point1_PointF_point2_Color_color1_Colo"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_PointF_point1_PointF_point2_Color_color1_Colo.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushconstructors\lineargradientbrush_22pointfamppoint1_pointfamppoint2_colora.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush, LinearGradientBrush class [GDI+],LinearGradientBrush constructor, LinearGradientBrush constructor [GDI+], LinearGradientBrush constructor [GDI+],LinearGradientBrush class, LinearGradientBrush.LinearGradientBrush, LinearGradientBrush.LinearGradientBrush(IN const PointF &,IN const PointF &,IN const Color &,IN const Color &), LinearGradientBrush.LinearGradientBrush(const PointF&,const PointF&,const Color&,const Color&), LinearGradientBrush::LinearGradientBrush, LinearGradientBrush::LinearGradientBrush(IN const PointF &,IN const PointF &,IN const Color &,IN const Color &), _gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_PointF_point1_PointF_point2_Color_color1_Colo, gdiplus._gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_PointF_point1_PointF_point2_Color_color1_Colo
req.header: gdiplusbrush.h
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
 - LinearGradientBrush::LinearGradientBrush
 - gdiplusbrush/LinearGradientBrush::LinearGradientBrush
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
 - LinearGradientBrush.LinearGradientBrush
---

## -description

Creates a <b>LinearGradientBrush::LinearGradientBrush</b> object from a set of boundary points and boundary colors.

## -parameters

### -param point1 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object that specifies the starting point of the gradient. The starting boundary line passes through the starting point.

### -param point2 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object that specifies the ending point of the gradient. The ending boundary line passes through the ending point.

### -param color1 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the starting boundary line of this linear gradient brush.

### -param color2 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the ending boundary line of this linear gradient brush.

## -remarks

The "directional line," an imaginary straight line, is defined by the starting point, <i>point1</i>, and the ending point, <i>point2</i>. The starting boundary of the gradient is a straight line that is perpendicular to the directional line and that passes through the starting point. The ending boundary of the gradient is a straight line that is parallel to the starting boundary line and that passes through the ending point. The gradient color is constant along lines that are parallel to the boundary lines. The gradient gradually changes from the starting color to the ending color along the directional line.

## Examples

The following example creates a linear gradient brush from a set of boundary points and boundary colors. The code then uses the brush to paint the interior of a rectangle.

```cpp
VOID Example_Construct02(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush(
      PointF(0.8f, 1.6f),
      PointF(3.0f, 2.4f),
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255));  // blue

   myGraphics.SetPageUnit(UnitInch);
   myGraphics.FillRectangle(&linGrBrush, 0, 0, 4, 3); 
}
```

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>
---
UID: NF:gdiplusbrush.LinearGradientBrush.LinearGradientBrush(constRectF&,constColor&,constColor&,REAL,BOOL)
title: LinearGradientBrush::LinearGradientBrush(IN const RectF &,IN const Color &,IN const Color &,IN REAL,IN BOOL) (gdiplusbrush.h)
description: Creates a LinearGradientBrush::LinearGradientBrush object from a rectangle and angle of direction. (overload 1/2)
helpviewer_keywords: ["LinearGradientBrush","LinearGradientBrush class [GDI+]","LinearGradientBrush constructor","LinearGradientBrush constructor [GDI+]","LinearGradientBrush constructor [GDI+]","LinearGradientBrush class","LinearGradientBrush.LinearGradientBrush","LinearGradientBrush.LinearGradientBrush(IN const RectF &","IN const Color &","IN const Color &","IN REAL","IN BOOL)","LinearGradientBrush.LinearGradientBrush(const Rect&","const Color&","const Color&","REAL","BOOL)","LinearGradientBrush::LinearGradientBrush","LinearGradientBrush::LinearGradientBrush(IN const RectF &","IN const Color &","IN const Color &","IN REAL","IN BOOL)","_gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_REAL_ang","gdiplus._gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_REAL_ang"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_REAL_ang.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushconstructors\lineargradientbrush_63rectfamprect_colorampcolor1_colorampco.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush, LinearGradientBrush class [GDI+],LinearGradientBrush constructor, LinearGradientBrush constructor [GDI+], LinearGradientBrush constructor [GDI+],LinearGradientBrush class, LinearGradientBrush.LinearGradientBrush, LinearGradientBrush.LinearGradientBrush(IN const RectF &,IN const Color &,IN const Color &,IN REAL,IN BOOL), LinearGradientBrush.LinearGradientBrush(const Rect&,const Color&,const Color&,REAL,BOOL), LinearGradientBrush::LinearGradientBrush, LinearGradientBrush::LinearGradientBrush(IN const RectF &,IN const Color &,IN const Color &,IN REAL,IN BOOL), _gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_REAL_ang, gdiplus._gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_REAL_ang
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

# LinearGradientBrush::LinearGradientBrush(IN const RectF &,IN const Color &,IN const Color &,IN REAL,IN BOOL)


## -description

Creates a <b>LinearGradientBrush::LinearGradientBrush</b> object from a rectangle and angle of direction.

## -parameters

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle that specifies the starting and ending points of the gradient. The upper-left corner of the rectangle is the starting point. The lower-right corner is the ending point.

### -param color1 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the starting boundary line of this linear gradient brush.

### -param color2 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the ending boundary line of this linear gradient brush.

### -param angle [in]

Type: <b>REAL</b>

Real number that, if <i>isAngleScalable</i> is <b>TRUE</b>, specifies the base angle from which the angle of the directional line is calculated, or that, if <i>isAngleScalable</i> is <b>FALSE</b>, specifies the angle of the directional line. The angle is measured from the top of the rectangle that is specified by <i>rect</i> and must be in degrees. The gradient follows the directional line.

### -param isAngleScalable [in]

Type: <b>BOOL</b>

<b>BOOL</b> value that specifies whether the angle is scalable. If <i>isAngleScalable</i> is <b>TRUE</b>, the angle of the directional line is scalable; otherwise, the angle is not scalable.

## -remarks

The "directional line," an imaginary straight line, is defined by the starting point (upper-left corner of the rectangle <i>rect</i>) and the angle <i>angle</i>. The starting boundary of the gradient is a straight line that is perpendicular to the directional line and that passes through the starting point. The ending boundary of the gradient is a straight line that is parallel to the starting boundary line and that passes through the ending point (lower-right corner of the rectangle <i>rect</i>). The gradient color is constant along lines that are parallel to the boundary lines. The gradient gradually changes from the starting color to the ending color along the directional line.

If <i>isAngleScalable</i> is <b>TRUE</b>, the base angle is scaled to produce the angle of the directional line:

ß = arctan( (width / height) tan(ø) )

where ß is the new angle of the directional line; width and height are the dimensions of the rectangle rect; and ø is the base angle <i>angle</i>. This relationship is valid only if angle is less than 90 degrees.

## -see-also

<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>

---
UID: NF:gdiplusbrush.LinearGradientBrush.LinearGradientBrush(constRectF&,constColor&,constColor&,LinearGradientMode)
title: LinearGradientBrush::LinearGradientBrush(IN const RectF &,IN const Color &,IN const Color &,IN LinearGradientMode) (gdiplusbrush.h)
description: Creates a LinearGradientBrush::LinearGradientBrush object based on a rectangle and mode of direction. (overload 2/2)
helpviewer_keywords: ["LinearGradientBrush","LinearGradientBrush class [GDI+]","LinearGradientBrush constructor","LinearGradientBrush constructor [GDI+]","LinearGradientBrush constructor [GDI+]","LinearGradientBrush class","LinearGradientBrush.LinearGradientBrush","LinearGradientBrush.LinearGradientBrush(IN const RectF &","IN const Color &","IN const Color &","IN LinearGradientMode)","LinearGradientBrush.LinearGradientBrush(const RectF&","const Color&","const Color&","LinearGradientMode)","LinearGradientBrush::LinearGradientBrush","LinearGradientBrush::LinearGradientBrush(IN const RectF &","IN const Color &","IN const Color &","IN LinearGradientMode)","_gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_LinearGr","gdiplus._gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_LinearGr"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_LinearGr.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushconstructors\lineargradientbrush_57rectfamprect_colorampcolor1_colorampco.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush, LinearGradientBrush class [GDI+],LinearGradientBrush constructor, LinearGradientBrush constructor [GDI+], LinearGradientBrush constructor [GDI+],LinearGradientBrush class, LinearGradientBrush.LinearGradientBrush, LinearGradientBrush.LinearGradientBrush(IN const RectF &,IN const Color &,IN const Color &,IN LinearGradientMode), LinearGradientBrush.LinearGradientBrush(const RectF&,const Color&,const Color&,LinearGradientMode), LinearGradientBrush::LinearGradientBrush, LinearGradientBrush::LinearGradientBrush(IN const RectF &,IN const Color &,IN const Color &,IN LinearGradientMode), _gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_LinearGr, gdiplus._gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_RectF_rect_Color_color1_Color_color2_LinearGr
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

# LinearGradientBrush::LinearGradientBrush(IN const RectF &,IN const Color &,IN const Color &,IN LinearGradientMode)


## -description

Creates a <b>LinearGradientBrush::LinearGradientBrush</b> object based on a rectangle and mode of direction.

## -parameters

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Reference to a rectangle that specifies the starting and ending points of the gradient. The direction of the gradient, specified by <i>mode</i>, affects how these points are defined. The dimensions of the rectangle affect the direction of the gradient for forward diagonal mode and backward diagonal mode.

### -param color1 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the starting boundary line of this linear gradient brush.

### -param color2 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the ending boundary line of this linear gradient brush.

### -param mode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-lineargradientmode">LinearGradientMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-lineargradientmode">LinearGradientMode</a> enumeration that specifies the direction of the gradient.

## -remarks

The starting boundary of the gradient is a straight line that either passes through the starting point or borders the rectangle <i>rect</i>. The ending boundary of the gradient is a straight line that is parallel to the starting boundary line and that either passes through the ending point or borders the rectangle. The "directional line," an imaginary straight line, is perpendicular to the boundary lines. The gradient color is constant along lines that are parallel to the boundary lines. The gradient gradually changes from the starting color to the ending color along the directional line. 

The mode affects the boundaries of the gradient: 

<ul>
<li>Vertical mode
							The boundary lines are parallel to the top (and bottom) of the rectangle <i>rect</i>. The starting and ending boundary lines are the top and bottom, respectively, of the rectangle <i>rect</i>. 

</li>
<li>Horizontal mode 
							The boundary lines are parallel to the left (and right) of the rectangle <i>rect</i>. The starting and ending boundary lines are the left and right, respectively, of the rectangle <i>rect</i>. 

</li>
<li>Forward diagonal mode 
							The boundary lines are parallel to the diagonal line that is defined by the upper-right corner and lower-left corner of the rectangle <i>rect</i>. The starting boundary line passes through the starting point (upper-left corner of the rectangle <i>rect</i>). The ending boundary line passes through the ending point (lower-right corner of the rectangle <i>rect</i>). Note that starting and ending points are opposites of the starting and ending points for backward diagonal mode. 

</li>
<li>Backward diagonal mode 
							The boundary lines are parallel to the diagonal line that is defined by the upper-left corner and lower-right corner of the rectangle <i>rect</i>. The starting boundary line passes through the starting point (upper-right corner of the rectangle <i>rect</i>). The ending boundary line passes through the ending point (lower-left corner of the rectangle <i>rect</i>). Note that starting and ending points are opposites of the starting and ending points for forward diagonal mode. 

</li>
</ul>

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-linear-gradient-use">Creating a Linear Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-lineargradientmode">LinearGradientMode</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>

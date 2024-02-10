---
UID: NF:gdiplusgraphics.Graphics.DrawDriverString
title: Graphics::DrawDriverString (gdiplusgraphics.h)
description: The Graphics::DrawDriverString method draws characters at the specified positions. The method gives the client complete control over the appearance of text. The method assumes that the client has already set up the format and layout to be applied.
helpviewer_keywords: ["DrawDriverString","DrawDriverString method [GDI+]","DrawDriverString method [GDI+]","Graphics class","Graphics class [GDI+]","DrawDriverString method","Graphics.DrawDriverString","Graphics::DrawDriverString","_gdiplus_CLASS_Graphics_DrawDriverString_text_length_font_brush_positions_flags_matrix_","gdiplus._gdiplus_CLASS_Graphics_DrawDriverString_text_length_font_brush_positions_flags_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawDriverString_text_length_font_brush_positions_flags_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\drawdriverstring.htm
ms.date: 12/05/2018
ms.keywords: DrawDriverString, DrawDriverString method [GDI+], DrawDriverString method [GDI+],Graphics class, Graphics class [GDI+],DrawDriverString method, Graphics.DrawDriverString, Graphics::DrawDriverString, _gdiplus_CLASS_Graphics_DrawDriverString_text_length_font_brush_positions_flags_matrix_, gdiplus._gdiplus_CLASS_Graphics_DrawDriverString_text_length_font_brush_positions_flags_matrix_
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
 - Graphics::DrawDriverString
 - gdiplusgraphics/Graphics::DrawDriverString
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
 - Graphics.DrawDriverString
---

# Graphics::DrawDriverString


## -description

The <b>Graphics::DrawDriverString</b> method draws characters at the specified positions. The method gives the client complete control over the appearance of text. The method assumes that the client has already set up the format and layout to be applied.

## -parameters

### -param text [in]

Type: <b>const UINT16*</b>

Pointer to an array of 16-bit values. If the <b>DriverStringOptionsCmapLookup</b> flag is set, each value specifies a Unicode character to be displayed. Otherwise, each value specifies an index to a font glyph that defines a character to be displayed.

### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of values in the 
					<i>text</i> array. The 
					<i>length</i> parameter can be set to 
					–1 if the string is null terminated.

### -param font [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object that specifies the family name, size, and style of the font that is to be applied to the string.

### -param brush [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to fill the string.

### -param positions [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

If the <b>DriverStringOptionsRealizedAdvance</b> flag is set, <i>positions</i> is a pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object that specifies the position of the first glyph. Otherwise, <i>positions</i> is an array of <b>PointF</b> objects, each of which specifies the origin of an individual glyph.

### -param flags [in]

Type: <b>INT</b>

Integer that specifies the options for the appearance of the string. This value must be an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-driverstringoptions">DriverStringOptions</a> enumeration or the result of a bitwise 
					<b>OR</b> applied to two or more of these elements.

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the transformation matrix to apply to each value in the 
					<i>text</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

This method does not support the handling of complex scripts and assumes that the client has set up all text layout in some other way. This method is useful for creating owner-drawn menu items. The client should use the 
				<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)">DrawString Methods</a> method for general purposes.

## -see-also

<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)">DrawString Methods</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-driverstringoptions">DriverStringOptions</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-measuredriverstring">Graphics::MeasureDriverString</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

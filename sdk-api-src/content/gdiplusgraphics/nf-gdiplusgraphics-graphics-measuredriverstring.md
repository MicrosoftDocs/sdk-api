---
UID: NF:gdiplusgraphics.Graphics.MeasureDriverString
title: Graphics::MeasureDriverString (gdiplusgraphics.h)
description: The Graphics::MeasureDriverString method measures the bounding box for the specified characters and their corresponding positions.
helpviewer_keywords: ["Graphics class [GDI+]","MeasureDriverString method","Graphics.MeasureDriverString","Graphics::MeasureDriverString","MeasureDriverString","MeasureDriverString method [GDI+]","MeasureDriverString method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_","gdiplus._gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\measuredriverstring.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],MeasureDriverString method, Graphics.MeasureDriverString, Graphics::MeasureDriverString, MeasureDriverString, MeasureDriverString method [GDI+], MeasureDriverString method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_, gdiplus._gdiplus_CLASS_Graphics_MeasureDriverString_text_length_font_positions_flags_matrix_boundingBox_
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
 - Graphics::MeasureDriverString
 - gdiplusgraphics/Graphics::MeasureDriverString
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
 - Graphics.MeasureDriverString
---

# Graphics::MeasureDriverString


## -description

The <b>Graphics::MeasureDriverString</b> method measures the bounding box for the specified characters and their corresponding positions.

## -parameters

### -param text [in]

Type: <b>const UINT16*</b>

Pointer to an array of 16-bit values. If the DriverStringOptionsCmapLookup flag is set, each value specifies a Unicode character to be displayed. Otherwise, each value specifies an index to a font glyph that defines a character to be displayed.

### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of values in the <i>text</i> array. The <i>length</i> parameter can be set to –1 if the string is null terminated.

### -param font [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object that specifies the family name, size, and style of the font to be applied to the string.

### -param positions [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

If the DriverStringOptionsRealizedAdvance flag is set, <i>positions</i> is a pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object that specifies the position of the first glyph. Otherwise, <i>positions</i> is an array of <b>PointF</b> objects, each of which specifies the origin of an individual glyph.

### -param flags [in]

Type: <b>INT</b>

Integer that specifies the options for the appearance of the string. This value must be an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-driverstringoptions">DriverStringOptions</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements.

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the transformation matrix to apply to each value in the <i>text</i> array.

### -param boundingBox [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that receives the rectangle that bounds the string.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-driverstringoptions">DriverStringOptions</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawdriverstring">Graphics::DrawDriverString</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>
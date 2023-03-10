---
UID: NF:gdiplusgraphics.Graphics.MeasureString(constWCHAR,INT,constFont,constSizeF&,constStringFormat,SizeF,INT,INT)
title: Graphics::MeasureString(IN const WCHAR,IN INT,IN const Font,IN const SizeF &,IN const StringFormat,OUT SizeF,OUT INT,OUT INT) (gdiplusgraphics.h)
description: The Graphics::MeasureString method measures the extent of the string in the specified font, format, and layout rectangle. (overload 1/3)
helpviewer_keywords: ["Graphics class [GDI+]","MeasureString method","Graphics.MeasureString","Graphics.MeasureString(IN const WCHAR","IN INT","IN const Font","IN const SizeF &","IN const StringFormat","OUT SizeF","OUT INT","OUT INT)","Graphics.MeasureString(const WCHAR*","INT","const Font*","const SizeF&","const StringFormat*","SizeF*","INT*","INT*)","Graphics::MeasureString","Graphics::MeasureString(IN const WCHAR","IN INT","IN const Font","IN const SizeF &","IN const StringFormat","OUT SizeF","OUT INT","OUT INT)","MeasureString","MeasureString method [GDI+]","MeasureString method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_MeasureString_string_length_font_layoutRectSize_stringFormat_size_codepoints","gdiplus._gdiplus_CLASS_Graphics_MeasureString_string_length_font_layoutRectSize_stringFormat_size_codepoints"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_MeasureString_string_length_font_layoutRectSize_stringFormat_size_codepoints.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsmeasurestringmethods\measurestring_56string_length_font_layoutrectsize_stri.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],MeasureString method, Graphics.MeasureString, Graphics.MeasureString(IN const WCHAR,IN INT,IN const Font,IN const SizeF &,IN const StringFormat,OUT SizeF,OUT INT,OUT INT), Graphics.MeasureString(const WCHAR*,INT,const Font*,const SizeF&,const StringFormat*,SizeF*,INT*,INT*), Graphics::MeasureString, Graphics::MeasureString(IN const WCHAR,IN INT,IN const Font,IN const SizeF &,IN const StringFormat,OUT SizeF,OUT INT,OUT INT), MeasureString, MeasureString method [GDI+], MeasureString method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_MeasureString_string_length_font_layoutRectSize_stringFormat_size_codepoints, gdiplus._gdiplus_CLASS_Graphics_MeasureString_string_length_font_layoutRectSize_stringFormat_size_codepoints
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
 - Graphics::MeasureString
 - gdiplusgraphics/Graphics::MeasureString
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
 - Graphics.MeasureString
---

# Graphics::MeasureString(IN const WCHAR,IN INT,IN const Font,IN const SizeF &,IN const StringFormat,OUT SizeF,OUT INT,OUT INT)


## -description

The <b>Graphics::MeasureString</b> method measures the extent of the string in the specified font, format, and layout rectangle.

## -parameters

### -param string [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string to be measured. 

<div class="alert"><b>Important</b>  For bidirectional languages, such as Arabic, the string length must not exceed 2046 characters.</div>
<div> </div>

### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of characters in the <i>string</i> array. The <i>length</i> parameter can be set to –1 if the string is null terminated.

### -param font [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object that specifies the family name, size, and style of the font that is applied to the string.

### -param layoutRectSize [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object that specifies the width and height of a rectangle that bounds the string.

### -param stringFormat [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object that specifies the layout information, such as alignment, trimming, tab stops, and so forth.

### -param size [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object that receives the width and height of the rectangle that bounds the string.

### -param codepointsFitted [out]

Type: <b>INT*</b>

Optional. Pointer to an <b>INT</b> that receives the number of characters that actually fit into the layout rectangle. The default value is a <b>NULL</b> pointer.

### -param linesFilled [out]

Type: <b>INT*</b>

Optional. Pointer to an <b>INT</b> that receives the number of lines that actually fit into the layout rectangle. The default value is a <b>NULL</b> pointer.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns OK, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)">DrawString Methods</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>

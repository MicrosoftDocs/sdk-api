---
UID: NF:gdiplusgraphics.Graphics.MeasureString(constWCHAR,INT,constFont,constRectF&,constStringFormat,RectF,INT,INT)
title: Graphics::MeasureString
description: The Graphics::MeasureString method measures the extent of the string in the specified font, format, and layout rectangle. (overload 3/3)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::MeasureString"]
ms.assetid: 95fe1f97-1978-4356-8707-f539adad3853
ms.date: 05/13/2019
ms.keywords: Graphics::MeasureString
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusgraphics.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Graphics::MeasureString
 - gdiplusgraphics/Graphics::MeasureString
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::MeasureString
---

# MeasureString(WCHAR*,INT,Font*,RectF&,StringFormat*,RectF*,INT*,INT*)


## -description

The **Graphics::MeasureString** method measures the extent of the string in the specified font, format, and layout rectangle.

## -parameters

### -param string

Pointer to a wide-character string to be measured.

**Important** For bidirectional languages, such as Arabic, the string length must not exceed 2046 characters.

### -param length

Integer that specifies the number of characters in the *string* array.
The *length* parameter can be set to -1 if the string is null terminated.

### -param font

Pointer to a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object that specifies the family name, size, and style of the font to be applied to the string.

### -param layoutRect

Reference to the rectangle that bounds the string.

### -param stringFormat

Pointer to a <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object that specifies the layout information, such as alignment, trimming, tab stops, and so forth.

### -param boundingBox

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that receives the rectangle that bounds the string.

### -param codepointsFitted

Optional. Pointer to an **INT** that receives the number of characters that actually fit into the layout rectangle.
The default value is a **NULL** pointer.

### -param linesFilled

Optional.
Pointer to an **INT** that receives the number of lines that fit into the layout rectangle.
The default value is a **NULL** pointer.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example measures the size of a string and then draws a rectangle that represents that size.

```cpp
VOID Example_MeasureString2(HDC hdc)
{
   Graphics graphics(hdc);
   // Set up the string.
   WCHAR string[] = L"Measure Text";
   Font font(L"Arial", 16);
   RectF layoutRect(0.0f, 0.0f, 100.0f, 50.0f);
   StringFormat format;
   format.SetAlignment(StringAlignmentFar);
   RectF boundRect;
   // Measure the string.
   graphics.MeasureString(string, 12, &font, layoutRect, &format, &boundRect);
   // Draw a rectangle that represents the size of the string.
   graphics.DrawRectangle(&Pen(Color(255, 0, 0, 0)), boundRect);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)">DrawString Methods</a>

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>

<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>

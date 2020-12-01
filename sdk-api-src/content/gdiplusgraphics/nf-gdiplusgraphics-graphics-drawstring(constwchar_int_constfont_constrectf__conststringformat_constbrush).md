---
UID: NF:gdiplusgraphics.Graphics.DrawString(constWCHAR,INT,constFont,constRectF&,constStringFormat,constBrush)
title: Graphics::DrawString
description: The Graphics::DrawString method draws a string based on a font, a layout rectangle, and a format.
tech.root: gdiplus
helpviewer_keywords: ["Graphics::DrawString"]
ms.assetid: ef1d9dc7-132f-4e0b-aba8-bc5a0c5d5d84
ms.date: 05/13/2019
ms.keywords: Graphics::DrawString
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
 - Graphics::DrawString
 - gdiplusgraphics/Graphics::DrawString
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawString
---

# DrawString(WCHAR*,INT,Font*,RectF&,StringFormat*,Brush*)


## -description

The **Graphics::DrawString** method draws a string based on a font, a layout rectangle, and a format.

## -parameters

### -param string

Pointer to a wide-character string to be drawn.

### -param length

Integer that specifies the number of characters in the *string* array.
The *length* parameter can be set to -1 if the string is null terminated.

### -param font

Pointer to a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object that specifies the font attributes (the family name, the size, and the style of the font) to use.

### -param layoutRect

Reference to a rectangle that bounds the string.

### -param stringFormat

Pointer to a <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object that specifies text layout information and display manipulations to be applied to the string.

### -param brush

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to fill the string.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

Note that GDI+ does not support PostScript fonts or OpenType fonts which do not have TrueType outlines.

When you use the GDI+ API, you must not allow your application to download arbitrary fonts from untrusted sources.
The operating system requires elevated privileges to assure that all installed fonts are trusted.

#### Examples

The following example uses the specified formatting to draw a string in a layout rectangle.

```cpp
VOID Example_DrawString(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a string.
   WCHAR string[] = L"Sample Text";
   
   // Initialize arguments.
   Font myFont(L"Arial", 16);
   RectF layoutRect(0.0f, 0.0f, 200.0f, 50.0f);
   StringFormat format;
   format.SetAlignment(StringAlignmentCenter);
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Draw string.
   graphics.DrawString(
   string,
   11,
   &myFont,
   layoutRect,
   &format,
   &blackBrush);

   // Draw layoutRect.
   graphics.DrawRectangle(&Pen(Color::Black, 3), layoutRect);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>

<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>
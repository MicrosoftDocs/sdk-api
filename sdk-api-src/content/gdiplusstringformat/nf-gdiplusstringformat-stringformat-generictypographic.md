---
UID: NF:gdiplusstringformat.StringFormat.GenericTypographic
title: StringFormat::GenericTypographic (gdiplusstringformat.h)
description: The StringFormat::GenericTypographic method creates a generic, typographic StringFormat object.
helpviewer_keywords: ["GenericTypographic","GenericTypographic method [GDI+]","GenericTypographic method [GDI+]","StringFormat class","StringFormat class [GDI+]","GenericTypographic method","StringFormat.GenericTypographic","StringFormat::GenericTypographic","_gdiplus_CLASS_StringFormat_GenericTypographic_","gdiplus._gdiplus_CLASS_StringFormat_GenericTypographic_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_GenericTypographic_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\generictypographic.htm
ms.date: 12/05/2018
ms.keywords: GenericTypographic, GenericTypographic method [GDI+], GenericTypographic method [GDI+],StringFormat class, StringFormat class [GDI+],GenericTypographic method, StringFormat.GenericTypographic, StringFormat::GenericTypographic, _gdiplus_CLASS_StringFormat_GenericTypographic_, gdiplus._gdiplus_CLASS_StringFormat_GenericTypographic_
req.header: gdiplusstringformat.h
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
 - StringFormat::GenericTypographic
 - gdiplusstringformat/StringFormat::GenericTypographic
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
 - StringFormat.GenericTypographic
---

# StringFormat::GenericTypographic


## -description

The <b>StringFormat::GenericTypographic</b> method creates a generic, typographic 
			<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object.

## -remarks

A generic, typographic 
				<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object has the following characteristics: 

<ul>
<li>String format flags StringFormatFlagsLineLimit, StringFormatFlagsNoClip, and StringFormatFlagsNoFitBlackBox are set. </li>
<li>Character alignment and line alignment are set to StringAlignmentNear. </li>
<li>Language ID is set to neutral language, which means that the current language associated with the calling thread is used. </li>
<li>String digit substitution is set to StringDigitSubstituteUser. </li>
<li>Hot key prefix is set to HotkeyPrefixNone. </li>
<li>Number of tab stops is set to zero. </li>
<li>String trimming is set to StringTrimmingNone. </li>
</ul>

#### Examples



The following example creates a generic, typographic 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object and then uses it to draw a formatted string. The code also draws the string's layout rectangle.


```cpp
VOID Example_GenericTypographic(HDC hdc)
{
   Graphics graphics(hdc);
   SolidBrush  solidBrush(Color(255, 255, 0, 0)); 
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 12, FontStyleRegular, UnitPoint);
   
   // Create a generic typographic StringFormat object.
   const StringFormat* pStringFormat = StringFormat::GenericTypographic();
   // Use the generic typographic StringFormat object 
   // in a call to DrawString.
  graphics.DrawString(
      L"Formatted by a generic typographic StringFormat object", 
      54,  // string length
      &font, 
      RectF(30, 30, 100, 120), 
      pStringFormat, 
      &solidBrush);
   // Draw the rectangle that encloses the text.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawRectangle(&pen, 30, 30, 100, 120);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hotkeyprefix">HotkeyPrefix</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringalignment">StringAlignment</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringdigitsubstitute">StringDigitSubstitute</a>



<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringformatflags">StringFormatFlags</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringtrimming">StringTrimming</a>

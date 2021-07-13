---
UID: NF:gdiplusstringformat.StringFormat.GenericDefault
title: StringFormat::GenericDefault (gdiplusstringformat.h)
description: The StringFormat::GenericDefault method creates a generic, default StringFormat object.
helpviewer_keywords: ["GenericDefault","GenericDefault method [GDI+]","GenericDefault method [GDI+]","StringFormat class","StringFormat class [GDI+]","GenericDefault method","StringFormat.GenericDefault","StringFormat::GenericDefault","_gdiplus_CLASS_StringFormat_GenericDefault_","gdiplus._gdiplus_CLASS_StringFormat_GenericDefault_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_GenericDefault_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\genericdefault.htm
ms.date: 12/05/2018
ms.keywords: GenericDefault, GenericDefault method [GDI+], GenericDefault method [GDI+],StringFormat class, StringFormat class [GDI+],GenericDefault method, StringFormat.GenericDefault, StringFormat::GenericDefault, _gdiplus_CLASS_StringFormat_GenericDefault_, gdiplus._gdiplus_CLASS_StringFormat_GenericDefault_
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
 - StringFormat::GenericDefault
 - gdiplusstringformat/StringFormat::GenericDefault
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
 - StringFormat.GenericDefault
---

# StringFormat::GenericDefault


## -description

The <b>StringFormat::GenericDefault</b> method creates a generic, default 
			<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object.

## -remarks

A generic, default 
				<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object has the following characteristics: 

<ul>
<li>No string format flags are set. </li>
<li>Character alignment and line alignment are set to StringAlignmentNear. </li>
<li>Language ID is set to neutral language, which means that the current language associated with the calling thread is used. </li>
<li>String digit substitution is set to StringDigitSubstituteUser. </li>
<li>Hot key prefix is set to HotkeyPrefixNone. </li>
<li>Number of tab stops is set to zero. </li>
<li>String trimming is set to StringTrimmingCharacter. </li>
</ul>

#### Examples



The following example creates a generic, default 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object and then uses it to draw a formatted string. The code also draws the string's layout rectangle.


```cpp
VOID Example_GenericDefault(HDC hdc)
{
   Graphics graphics(hdc);

   SolidBrush  solidBrush(Color(255, 255, 0, 0)); 
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 12, FontStyleRegular, UnitPoint);
   
   // Create a generic StringFormat object.
   const StringFormat* pStringFormat = StringFormat::GenericDefault();

   // Use the generic StringFormat object in a call to DrawString.
  graphics.DrawString(
      L"This text was formatted by a generic StringFormat object.", 
      57,  // string length
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

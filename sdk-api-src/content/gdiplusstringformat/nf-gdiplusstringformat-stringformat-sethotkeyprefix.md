---
UID: NF:gdiplusstringformat.StringFormat.SetHotkeyPrefix
title: StringFormat::SetHotkeyPrefix (gdiplusstringformat.h)
description: The StringFormat::SetHotkeyPrefix method sets the type of processing that is performed on a string when the hot key prefix, an ampersand (&), is encountered.
helpviewer_keywords: ["SetHotkeyPrefix","SetHotkeyPrefix method [GDI+]","SetHotkeyPrefix method [GDI+]","StringFormat class","StringFormat class [GDI+]","SetHotkeyPrefix method","StringFormat.SetHotkeyPrefix","StringFormat::SetHotkeyPrefix","_gdiplus_CLASS_StringFormat_SetHotkeyPrefix_hotkeyPrefix_","gdiplus._gdiplus_CLASS_StringFormat_SetHotkeyPrefix_hotkeyPrefix_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetHotkeyPrefix_hotkeyPrefix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\sethotkeyprefix.htm
ms.date: 12/05/2018
ms.keywords: SetHotkeyPrefix, SetHotkeyPrefix method [GDI+], SetHotkeyPrefix method [GDI+],StringFormat class, StringFormat class [GDI+],SetHotkeyPrefix method, StringFormat.SetHotkeyPrefix, StringFormat::SetHotkeyPrefix, _gdiplus_CLASS_StringFormat_SetHotkeyPrefix_hotkeyPrefix_, gdiplus._gdiplus_CLASS_StringFormat_SetHotkeyPrefix_hotkeyPrefix_
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
 - StringFormat::SetHotkeyPrefix
 - gdiplusstringformat/StringFormat::SetHotkeyPrefix
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
 - StringFormat.SetHotkeyPrefix
---

# StringFormat::SetHotkeyPrefix


## -description

The <b>StringFormat::SetHotkeyPrefix</b> method sets the type of processing that is performed on a string when the hot key prefix, an ampersand (&amp;), is encountered. The ampersand is called the hot key prefix and can be used to designate certain keys as hot keys.

## -parameters

### -param hotkeyPrefix [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hotkeyprefix">HotkeyPrefix</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hotkeyprefix">HotkeyPrefix</a> enumeration that specifies how to process the hot key prefix.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Hot keys, also called access keys, are keys that are programmed to provide an end user with keyboard shortcuts to functionality and are activated by pressing the ALT key. The keys are application dependent and are identified by an underscored letter, typically in a menu name or menu item; for example, when you press ALT, the letter F of the 
				<b>File</b> menu is underscored. The F key is a shortcut to display the 
				<b>File</b> menu.

A client programmer designates a hot key in an application by using the hot key prefix, an ampersand (&amp;), in a string that typically is displayed as the name of a menu or an item in a menu and by using the 
				<b>StringFormat::SetHotkeyPrefix</b> method to set the appropriate type of processing. When a character in a string is preceded with an ampersand, the key that corresponds to the character becomes a hot key during the processing that occurs when the string is drawn on the display device. The ampersand is called a hot key prefix because it precedes the character to be activated. If HotkeyPrefixNone is passed to <b>StringFormat::SetHotkeyPrefix</b>, no processing of the hot key prefix occurs.

<div class="alert"><b>Note</b>  The term 
				<i>hot key</i> is used synonymously here with the term 
				<i>access key</i>. The term 
				<i>hot key</i> may have a different meaning in other Windows APIs.</div>
<div> </div>

#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object and sets the type of hot key prefix processing to be performed on the string. The code then uses the 
						<b>StringFormat</b> object to draw a string that contains the hot key prefix character. The code also draws the string's layout rectangle.


```cpp
VOID Example_SetHotkeyPrefix(HDC hdc)
{
   Graphics graphics(hdc);

   SolidBrush  solidBrush(Color(255, 255, 0, 0)); 
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   StringFormat stringFormat;
   stringFormat.SetHotkeyPrefix(HotkeyPrefixShow);

   graphics.DrawString(
      L"This &text has some &underlined characters.", 
      43,  // string length
      &font, 
      RectF(30, 30, 160, 200), 
      &stringFormat, 
      &solidBrush);

   // Draw the rectangle that encloses the text.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawRectangle(&pen, 30, 30, 160, 200);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hotkeyprefix">HotkeyPrefix</a>



<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-gethotkeyprefix">StringFormat::GetHotkeyPrefix</a>
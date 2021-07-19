---
UID: NF:gdiplusstringformat.StringFormat.GetLastStatus
title: StringFormat::GetLastStatus (gdiplusstringformat.h)
description: The StringFormat::GetLastStatus method returns a value that indicates the nature of this StringFormat object's most recent method failure.
helpviewer_keywords: ["GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","StringFormat class","StringFormat class [GDI+]","GetLastStatus method","StringFormat.GetLastStatus","StringFormat::GetLastStatus","_gdiplus_CLASS_StringFormat_GetLastStatus_","gdiplus._gdiplus_CLASS_StringFormat_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\getlaststatus_15.htm
ms.date: 12/05/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],StringFormat class, StringFormat class [GDI+],GetLastStatus method, StringFormat.GetLastStatus, StringFormat::GetLastStatus, _gdiplus_CLASS_StringFormat_GetLastStatus_, gdiplus._gdiplus_CLASS_StringFormat_GetLastStatus_
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
 - StringFormat::GetLastStatus
 - gdiplusstringformat/StringFormat::GetLastStatus
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
 - StringFormat.GetLastStatus
---

# StringFormat::GetLastStatus


## -description

The <b>StringFormat::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object's most recent method failure.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The <b>StringFormat::GetLastStatus</b> method returns an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If no methods invoked on this 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object have failed since the previous call to <b>StringFormat::GetLastStatus</b>, then <b>StringFormat::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object has failed since the previous call to <b>StringFormat::GetLastStatus</b>, then <b>StringFormat::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.

## -remarks

You can call <b>StringFormat::GetLastStatus</b> immediately after constructing a 
				<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object to determine whether the constructor succeeded.

The first time you call the <b>StringFormat::GetLastStatus</b> method of a 
				<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>StringFormat</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object, calls two 
						<b>StringFormat</b> methods, and then checks the status to see if an error occurred during the construction or either of the method calls.


```cpp
StringFormat stringFormat;
stringFormat.SetAlignment(StringAlignmentCenter);
HotkeyPrefix hotkeyPrefix = stringFormat.GetHotkeyPrefix();

if (stringFormat.GetLastStatus() == Ok)
{
   // There have been no errors since the previous call to GetLastStatus.
}
else
{
   // An error occurred since the previous call to GetLastStatus.
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringformatflags">StringFormatFlags</a>

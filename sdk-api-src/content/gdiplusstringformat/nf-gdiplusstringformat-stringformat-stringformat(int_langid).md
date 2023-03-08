---
UID: NF:gdiplusstringformat.StringFormat.StringFormat(INT,LANGID)
title: StringFormat::StringFormat(IN INT,IN LANGID) (gdiplusstringformat.h)
description: Creates a StringFormat object based on string format flags and a language.
helpviewer_keywords: ["StringFormat","StringFormat class [GDI+]","StringFormat constructor","StringFormat constructor [GDI+]","StringFormat constructor [GDI+]","StringFormat class","StringFormat.StringFormat","StringFormat.StringFormat(IN INT","IN LANGID)","StringFormat.StringFormat(INT","LANGID)","StringFormat::StringFormat","StringFormat::StringFormat(IN INT","IN LANGID)","_gdiplus_CLASS_StringFormat_StringFormat_formatFlags_language_","gdiplus._gdiplus_CLASS_StringFormat_StringFormat_formatFlags_language_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_StringFormat_formatFlags_language_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatconstructors\stringformat_22formatflags_language.htm
ms.date: 12/05/2018
ms.keywords: StringFormat, StringFormat class [GDI+],StringFormat constructor, StringFormat constructor [GDI+], StringFormat constructor [GDI+],StringFormat class, StringFormat.StringFormat, StringFormat.StringFormat(IN INT,IN LANGID), StringFormat.StringFormat(INT,LANGID), StringFormat::StringFormat, StringFormat::StringFormat(IN INT,IN LANGID), _gdiplus_CLASS_StringFormat_StringFormat_formatFlags_language_, gdiplus._gdiplus_CLASS_StringFormat_StringFormat_formatFlags_language_
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
 - StringFormat::StringFormat
 - gdiplusstringformat/StringFormat::StringFormat
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
 - StringFormat.StringFormat
---

# StringFormat::StringFormat(IN INT,IN LANGID)


## -description

Creates a <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object based on string format flags and a language.

## -parameters

### -param formatFlags [in]

Type: <b>INT</b>

Optional. Value that specifies the format flags that control most of the characteristics of the <a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object. The flags are set by applying a bitwise 
					<b>OR</b> to elements of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringformatflags">StringFormatFlags</a> enumeration. The default value is 0 (no flags set).

### -param language [in]

Type: <b>LANGID</b>

Optional. Sixteen-bit value that specifies the language to use. The default value is LANG_NEUTRAL, which is the user's default language.

## -remarks

When specifying LANG_NEUTRAL as the language ID, it is common practice to pass just LANG_NEUTRAL as in the following example: 

<code>stat = FontFamily.GetFamilyName(name, LANG_NEUTRAL);</code>

If you are specifying a language other than LANG_NEUTRAL, use <a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a> to create the language and sublanguage combination as in the following example:

<code>LANGID language = MAKELANGID(LANG_CHINESE, SUBLANG_CHINESE_TRADITIONAL);</code>

For a list of the available languages and sublanguages, see Winnt.h.

## -see-also

<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringformatflags">StringFormatFlags</a>
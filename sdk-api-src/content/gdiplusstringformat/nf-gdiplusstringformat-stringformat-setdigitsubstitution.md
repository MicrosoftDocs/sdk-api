---
UID: NF:gdiplusstringformat.StringFormat.SetDigitSubstitution
title: StringFormat::SetDigitSubstitution (gdiplusstringformat.h)
description: The StringFormat::SetDigitSubstitution method sets the digit substitution method and the language that corresponds to the digit substitutes.
helpviewer_keywords: ["SetDigitSubstitution","SetDigitSubstitution method [GDI+]","SetDigitSubstitution method [GDI+]","StringFormat class","StringFormat class [GDI+]","SetDigitSubstitution method","StringFormat.SetDigitSubstitution","StringFormat::SetDigitSubstitution","_gdiplus_CLASS_StringFormat_SetDigitSubstitution_language_substitute_","gdiplus._gdiplus_CLASS_StringFormat_SetDigitSubstitution_language_substitute_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetDigitSubstitution_language_substitute_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\setdigitsubstitution.htm
ms.date: 12/05/2018
ms.keywords: SetDigitSubstitution, SetDigitSubstitution method [GDI+], SetDigitSubstitution method [GDI+],StringFormat class, StringFormat class [GDI+],SetDigitSubstitution method, StringFormat.SetDigitSubstitution, StringFormat::SetDigitSubstitution, _gdiplus_CLASS_StringFormat_SetDigitSubstitution_language_substitute_, gdiplus._gdiplus_CLASS_StringFormat_SetDigitSubstitution_language_substitute_
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
 - StringFormat::SetDigitSubstitution
 - gdiplusstringformat/StringFormat::SetDigitSubstitution
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
 - StringFormat.SetDigitSubstitution
---

# StringFormat::SetDigitSubstitution


## -description

The <b>StringFormat::SetDigitSubstitution</b> method sets the digit substitution method and the language that corresponds to the digit substitutes.

## -parameters

### -param language [in]

Type: <b>LANGID</b>

Sixteen-bit value that forms a NLS language identifier. The identifier specifies the language associated with the substitute digits. For example, if this 
					<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object uses Arabic substitution digits, then this method will return a value that indicates an Arabic language. An NLS language identifier is constructed by the MAKELANGID macro, declared in Winnt.h.

### -param substitute [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringdigitsubstitute">StringDigitSubstitute</a></b>

Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringdigitsubstitute">StringDigitSubstitute</a> enumeration that specifies the digit substitution method to be used.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The digit substitution method, specified by an element of the 
				<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringdigitsubstitute">StringDigitSubstitute</a> enumeration, replaces, in a string, Western European digits with digits that correspond to a user's locale or language.

When specifying LANG_NEUTRAL as the language ID, it is common practice to pass just LANG_NEUTRAL as in the following example:

<code>stat = FontFamily.GetFamilyName(name, LANG_NEUTRAL);</code>

If you are specifying a language other than LANG_NEUTRAL, use MAKELANGID to create the language and sublanguage combination as in the following example: 

<code>LANGID language = MAKELANGID(LANG_CHINESE, SUBLANG_CHINESE_TRADITIONAL);</code>

For a list of the available languages and sublanguages, see Winnt.h.
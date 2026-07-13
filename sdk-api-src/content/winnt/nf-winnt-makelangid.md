---
UID: NF:winnt.MAKELANGID
title: MAKELANGID macro (winnt.h)
description: Creates a language identifier from a primary language identifier and a sublanguage identifier.
helpviewer_keywords: ["MAKELANGID","MAKELANGID macro [Internationalization for Windows Applications]","_win32_MAKELANGID","intl.makelangid","winnt/MAKELANGID"]
old-location: intl\makelangid.htm
tech.root: Intl
ms.assetid: cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3
ms.date: 07/01/2025
ms.keywords: MAKELANGID, MAKELANGID macro [Internationalization for Windows Applications], _win32_MAKELANGID, intl.makelangid, winnt/MAKELANGID
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAKELANGID
 - winnt/MAKELANGID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - MAKELANGID
---

# MAKELANGID macro

## -syntax

```cpp
WORD MAKELANGID(
    USHORT p,
    USHORT s
);
```

## -returns

Type: **WORD**

Returns the language identifier.

> [!IMPORTANT]
> Language identifier constants are deprecated and their use is discouraged. Use of locale names instead of locale identifiers is always preferable. See the documentation for <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>.

## -description

Creates a <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> from a primary language identifier and a sublanguage identifier.

## -parameters

### -param p

Primary language identifier. This identifier can be a predefined value or a value for a user-defined primary language. For a user-defined language, the identifier is a value in the range 0x0200 to 0x03FF. All other values are reserved for operating system use. For more information, see <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a>.

### -param s

Sublanguage identifier. This parameter can be a predefined sublanguage identifier or a user-defined sublanguage. For a user-defined sublanguage, the identifier is a value in the range 0x20 to 0x3F. All other values are reserved for operating system use. For more information, see <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a>.

## -remarks

The following table shows combinations of <i>usPrimaryLanguage</i> and <i>usSubLanguage</i> that have special meaning.

<table>
<tr>
<th>Primary language identifier</th>
<th>Sublanguage identifier</th>
<th>Meaning</th>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_NEUTRAL</td>
<td>Language neutral</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_DEFAULT</td>
<td>User default language</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_SYS_DEFAULT</td>
<td>System default language</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_CUSTOM_DEFAULT</td>
<td><b>Windows Vista and later:</b> Default custom locale</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_CUSTOM_UNSPECIFIED</td>
<td><b>Windows Vista and later:</b> Unspecified custom locale</td>
</tr>
<tr>
<td>LANG_NEUTRAL</td>
<td>SUBLANG_UI_CUSTOM_DEFAULT</td>
<td><b>Windows Vista and later:</b> Default custom Multilingual User Interface locale</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesa">EnumSystemLocales</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="/windows/desktop/api/winnt/nf-winnt-primarylangid">PRIMARYLANGID</a>



<a href="/windows/desktop/api/winnt/nf-winnt-sublangid">SUBLANGID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>

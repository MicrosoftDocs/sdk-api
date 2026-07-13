---
UID: NC:winnls.LANGGROUPLOCALE_ENUMPROCA
title: LANGGROUPLOCALE_ENUMPROCA (winnls.h)
description: An application-defined callback function that processes enumerated language group locale information provided by the EnumLanguageGroupLocales function. (ANSI)
helpviewer_keywords: ["LANGGROUPLOCALE_ENUMPROC","LANGGROUPLOCALE_ENUMPROC callback","LANGGROUPLOCALE_ENUMPROC callback function [Internationalization for Windows Applications]","LANGGROUPLOCALE_ENUMPROCA","LANGGROUPLOCALE_ENUMPROCW","_win32_EnumLanguageGroupLocalesProc","intl.enumlanguagegrouplocalesproc","winnls/LANGGROUPLOCALE_ENUMPROC"]
old-location: intl\enumlanguagegrouplocalesproc.htm
tech.root: Intl
ms.assetid: e422c61f-7a97-4f95-8592-22a1eb5f616b
ms.date: 12/05/2018
ms.keywords: LANGGROUPLOCALE_ENUMPROC, LANGGROUPLOCALE_ENUMPROC callback, LANGGROUPLOCALE_ENUMPROC callback function [Internationalization for Windows Applications], LANGGROUPLOCALE_ENUMPROCA, LANGGROUPLOCALE_ENUMPROCW, _win32_EnumLanguageGroupLocalesProc, intl.enumlanguagegrouplocalesproc, winnls/LANGGROUPLOCALE_ENUMPROC
req.header: winnls.h
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
 - LANGGROUPLOCALE_ENUMPROCA
 - winnls/LANGGROUPLOCALE_ENUMPROCA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winnls.h
api_name:
 - LANGGROUPLOCALE_ENUMPROC
---

# LANGGROUPLOCALE_ENUMPROCA callback function


## -description

An application-defined callback function that processes enumerated language group locale information provided by the <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa">EnumLanguageGroupLocales</a> function. The LANGGROUPLOCALE_ENUMPROC type defines a pointer to this callback function. <b>EnumLanguageGroupLocalesProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

### -param unnamedParam2

### -param unnamedParam3

### -param unnamedParam4

#### - LanguageGroup [in]

Identifier of the language group. This parameter can have one of the following values:

<ul>
<li>LGRPID_ARABIC</li>
<li>LGRPID_ARMENIAN</li>
<li>LGRPID_BALTIC</li>
<li>LGRPID_CENTRAL_EUROPE</li>
<li>LGRPID_CYRILLIC</li>
<li>LGRPID_GEORGIAN</li>
<li>LGRPID_GREEK</li>
<li>LGRPID_HEBREW</li>
<li>LGRPID_INDIC</li>
<li>LGRPID_JAPANESE</li>
<li>LGRPID_KOREAN
</li>
<li>LGRPID_SIMPLIFIED_CHINESE</li>
<li>LGRPID_TRADITIONAL_CHINESE</li>
<li>LGRPID_THAI</li>
<li>LGRPID_TURKIC</li>
<li>LGRPID_TURKISH</li>
<li>LGRPID_VIETNAMESE</li>
<li>LGRPID_WESTERN_EUROPE</li>
</ul>

#### - Locale [in]


<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-invariant">LOCALE_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
</ul>
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

<ul>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>

#### - lParam [in]

Application-defined value passed to the <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa">EnumLanguageGroupLocales</a> function. This parameter can be used for error checking.


#### - lpLocaleString [in]

Pointer to a buffer containing a null-terminated locale identifier string.

## -returns

Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> otherwise.

## -remarks

An <b>EnumLanguageGroupLocalesProc</b> function can carry out any desired task. The application registers this function by passing its address to the <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa">EnumLanguageGroupLocales</a> function.





> [!NOTE]
> The winnls.h header defines LANGGROUPLOCALE_ENUMPROC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa">EnumLanguageGroupLocales</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlanguagegroupsa">EnumSystemLanguageGroups</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>

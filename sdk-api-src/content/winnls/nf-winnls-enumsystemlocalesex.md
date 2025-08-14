---
UID: NF:winnls.EnumSystemLocalesEx
title: EnumSystemLocalesEx function (winnls.h)
description: Enumerates the locales that are either installed on or supported by an operating system.Note  The application should call this function in preference to EnumSystemLocales if designed to run only on Windows Vista and later.
helpviewer_keywords: ["EnumSystemLocalesEx","EnumSystemLocalesEx function [Internationalization for Windows Applications]","_win32_EnumSystemLocalesEx","intl.enumsystemlocalesex","winnls/EnumSystemLocalesEx"]
old-location: intl\enumsystemlocalesex.htm
tech.root: Intl
ms.assetid: 74b1b453-66e9-4724-a956-26cea2d7d744
ms.date: 12/05/2018
ms.keywords: EnumSystemLocalesEx, EnumSystemLocalesEx function [Internationalization for Windows Applications], _win32_EnumSystemLocalesEx, intl.enumsystemlocalesex, winnls/EnumSystemLocalesEx
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumSystemLocalesEx
 - winnls/EnumSystemLocalesEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - api-ms-win-core-localization-l1-2-3.dll
api_name:
 - EnumSystemLocalesEx
---

# EnumSystemLocalesEx function


## -description

Enumerates the locales that are either installed on or supported by an operating system.
<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesa">EnumSystemLocales</a> if designed to run only on Windows Vista and later.</div><div> </div>

## -parameters

### -param lpLocaleEnumProcEx [in]

Pointer to an application-defined callback function. The <b>EnumSystemLocalesEx</b> function enumerates locales by making repeated calls to this callback function. For more information, see <a href="/windows/desktop/api/winnls/nc-winnls-locale_enumprocex">EnumLocalesProcEx</a>.

### -param dwFlags [in]

Flags identifying the locales to enumerate. The flags can be used singly or combined using a binary OR. If the application specifies 0 for this parameter, the function behaves as for <a href="/windows/desktop/Intl/locale-all">LOCALE_ALL</a>.

- <a href="/windows/desktop/Intl/locale-all">LOCALE_ALL</a>
- <a href="/windows/desktop/Intl/locale-alternate-sorts">LOCALE_ALTERNATE_SORTS</a>; see Remarks</li>
- <a href="/windows/desktop/Intl/locale-neutraldata">LOCALE_NEUTRALDATA</a>
- <a href="/windows/desktop/Intl/locale-supplemental">LOCALE_SUPPLEMENTAL</a>
- <a href="/windows/desktop/Intl/locale-windows">LOCALE_WINDOWS</a>
- [LOCALE_SPECIFICDATA](/windows/win32/intl/locale-specificdata)

### -param lParam [in]

An application-provided parameter to be passed to the callback function. This is especially useful for multi-threaded applications.

### -param lpReserved [in, optional]

Reserved; must be <b>NULL</b>.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function enumerates locales by passing locale names, one at a time, to the application-defined callback function specified by <i>lpLocaleEnumProcEx</i>. Enumeration continues until all installed or supported names have been passed to the callback function or the callback function returns <b>FALSE</b>.

The choices for the <i>dwFlags</i> parameter are different from those for <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesa">EnumSystemLocales</a>, which must distinguish between installed and supported locales.

If <i>dwFlags</i> specifies <a href="/windows/desktop/Intl/locale-alternate-sorts">LOCALE_ALTERNATE_SORTS</a>, the callback function is called for every locale that represents an alternate sort order. For example, Spanish (Spain) defaults to international sort order, but traditional sort order is available for an alternate sort. German (Germany) defaults to dictionary sort order, but there is an alternate phone book sort order available.


#### Examples

An example showing the use of this function can be found in <a href="/windows/desktop/Intl/nls--name-based-apis-sample">NLS: Name-based APIs Sample</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winnls/nc-winnls-locale_enumprocex">EnumLocalesProcEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesa">EnumSystemLocales</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
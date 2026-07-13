---
UID: NF:winnls.EnumSystemLocalesW
title: EnumSystemLocalesW function (winnls.h)
description: Enumerates the locales that are either installed on or supported by an operating system.Note  For interoperability reasons, the application should prefer the EnumSystemLocalesEx function to EnumSystemLocales because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that will be run only on Windows Vista and later should use EnumSystemLocalesEx. (Unicode)
helpviewer_keywords: ["EnumSystemLocales", "EnumSystemLocales function [Internationalization for Windows Applications]", "EnumSystemLocalesW", "LCID_ALTERNATE_SORTS", "LCID_INSTALLED", "LCID_SUPPORTED", "_win32_EnumSystemLocales", "intl.enumsystemlocales", "winnls/EnumSystemLocales", "winnls/EnumSystemLocalesW"]
old-location: intl\enumsystemlocales.htm
tech.root: Intl
ms.assetid: e6341460-3c4e-4040-8b49-3eb7d279e571
ms.date: 12/05/2018
ms.keywords: EnumSystemLocales, EnumSystemLocales function [Internationalization for Windows Applications], EnumSystemLocalesA, EnumSystemLocalesW, LCID_ALTERNATE_SORTS, LCID_INSTALLED, LCID_SUPPORTED, _win32_EnumSystemLocales, intl.enumsystemlocales, winnls/EnumSystemLocales, winnls/EnumSystemLocalesA, winnls/EnumSystemLocalesW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumSystemLocalesW (Unicode) and EnumSystemLocalesA (ANSI)
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
 - EnumSystemLocalesW
 - winnls/EnumSystemLocalesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - EnumSystemLocales
 - EnumSystemLocalesA
 - EnumSystemLocalesW
---

# EnumSystemLocalesW function


## -description

Enumerates the locales that are either installed on or supported by an operating system.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a> function to <b>EnumSystemLocales</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that will be run only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>.</div><div> </div>

## -parameters

### -param lpLocaleEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317822(v=vs.85)">EnumLocalesProc</a>.

### -param dwFlags [in]

Flags specifying the locale identifiers to enumerate. The flags can be used singly or combined using a binary OR. If the application specifies 0 for this parameter, the function behaves as for LCID_SUPPORTED.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LCID_INSTALLED"></a><a id="lcid_installed"></a><dl>
<dt><b>LCID_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only installed locale identifiers. This value cannot be used with LCID_SUPPORTED.

</td>
</tr>
<tr>
<td width="40%"><a id="LCID_SUPPORTED"></a><a id="lcid_supported"></a><dl>
<dt><b>LCID_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all supported locale identifiers. This value cannot be used with LCID_INSTALLED.

</td>
</tr>
<tr>
<td width="40%"><a id="LCID_ALTERNATE_SORTS"></a><a id="lcid_alternate_sorts"></a><dl>
<dt><b>LCID_ALTERNATE_SORTS</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only the alternate sort locale identifiers. If this value is used with either LCID_INSTALLED or LCID_SUPPORTED, the installed or supported locales are retrieved, as well as the alternate sort locale identifiers.

</td>
</tr>
</table>

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

The function enumerates locales by passing locale identifiers, one at a time, to the specified application-defined callback function. This continues until all of the installed or supported locale identifiers have been passed to the callback function or the callback function returns <b>FALSE</b>.





> [!NOTE]
> The winnls.h header defines EnumSystemLocales as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd317822(v=vs.85)">EnumLocalesProc</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesex">EnumSystemLocalesEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>

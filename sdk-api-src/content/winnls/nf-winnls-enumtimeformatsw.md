---
UID: NF:winnls.EnumTimeFormatsW
title: EnumTimeFormatsW function (winnls.h)
description: Enumerates the time formats that are available for a locale specified by identifier.Note  For interoperability reasons, the application should prefer the EnumTimeFormatsEx function to EnumTimeFormats because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use EnumTimeFormatsEx. (Unicode)
helpviewer_keywords: ["0", "EnumTimeFormats", "EnumTimeFormats function [Internationalization for Windows Applications]", "EnumTimeFormatsW", "LOCAL_USE_CP_ACP", "TIME_NOSECONDS", "_win32_EnumTimeFormats", "intl.enumtimeformats", "winnls/EnumTimeFormats", "winnls/EnumTimeFormatsW"]
old-location: intl\enumtimeformats.htm
tech.root: Intl
ms.assetid: ad0fe26f-b915-4903-9335-4b268a889c80
ms.date: 12/05/2018
ms.keywords: 0, EnumTimeFormats, EnumTimeFormats function [Internationalization for Windows Applications], EnumTimeFormatsA, EnumTimeFormatsW, LOCAL_USE_CP_ACP, TIME_NOSECONDS, _win32_EnumTimeFormats, intl.enumtimeformats, winnls/EnumTimeFormats, winnls/EnumTimeFormatsA, winnls/EnumTimeFormatsW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumTimeFormatsW (Unicode) and EnumTimeFormatsA (ANSI)
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
 - EnumTimeFormatsW
 - winnls/EnumTimeFormatsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumTimeFormats
 - EnumTimeFormatsA
 - EnumTimeFormatsW
---

# EnumTimeFormatsW function


## -description

Enumerates the time formats that are available for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-enumtimeformatsex">EnumTimeFormatsEx</a> function to <b>EnumTimeFormats</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-enumtimeformatsex">EnumTimeFormatsEx</a>.</div><div> </div>

## -parameters

### -param lpTimeFmtEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317832(v=vs.85)">EnumTimeFormatsProc</a>.

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale for which to retrieve time format information. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

### -param dwFlags [in]

The time format. This parameter can specify a combination of any of the following values.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Use the current user's long time format.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_NOSECONDS"></a><a id="time_noseconds"></a><dl>
<dt><b>TIME_NOSECONDS</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 7 and later</b>: Use the current user's short time format.

<div class="alert"><b>Note</b>  This value will not work with the ANSI version of this function, <b>EnumTimeFormatsA</b>.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="LOCAL_USE_CP_ACP"></a><a id="local_use_cp_acp"></a><dl>
<dt><b>LOCAL_USE_CP_ACP</b></dt>
</dl>
</td>
<td width="60%">
Specified with the ANSI version of this function, <b>EnumTimeFormatsA</b> (not recommended), to use the system default Windows ANSI code page (ACP) instead of the locale code page.

</td>
</tr>
</table>

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

The function enumerates the time formats by passing a pointer to a buffer containing a time format to an application-defined callback function. The first value in the enumeration is always the user default (override) value. The function continues enumeration until the last time format is found or the callback function returns <b>FALSE</b>. 


This function can enumerate data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the call can succeed because the system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark ("?"). 
Note that any new values for <i>dwFlags</i> introduced in the future will not work with the ANSI version.





> [!NOTE]
> The winnls.h header defines EnumTimeFormats as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumtimeformatsex">EnumTimeFormatsEx</a>



<a href="/previous-versions/windows/desktop/legacy/dd317832(v=vs.85)">EnumTimeFormatsProc</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>

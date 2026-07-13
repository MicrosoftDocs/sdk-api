---
UID: NF:winnls.SetLocaleInfoA
title: SetLocaleInfoA function (winnls.h)
description: Sets an item of information in the user override portion of the current locale. This function does not set the system defaults. (ANSI)
helpviewer_keywords: ["SetLocaleInfoA", "winnls/SetLocaleInfoA"]
old-location: intl\setlocaleinfo.htm
tech.root: Intl
ms.assetid: 96e031cb-0d9f-4556-b9b3-3451d8f80da5
ms.date: 12/05/2018
ms.keywords: SetLocaleInfo, SetLocaleInfo function [Internationalization for Windows Applications], SetLocaleInfoA, SetLocaleInfoW, _win32_SetLocaleInfo, intl.setlocaleinfo, winnls/SetLocaleInfo, winnls/SetLocaleInfoA, winnls/SetLocaleInfoW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetLocaleInfoW (Unicode) and SetLocaleInfoA (ANSI)
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
 - SetLocaleInfoA
 - winnls/SetLocaleInfoA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - SetLocaleInfo
 - SetLocaleInfoA
 - SetLocaleInfoW
---

# SetLocaleInfoA function


## -description

Sets an item of information in the user override portion of the current locale. This function does not set the system defaults.
<div class="alert"><b>Caution</b>  Because this function modifies values for all applications, it should only be called by the regional and language options functionality of Control Panel, or a similar utility. If making an international change to system parameters, the calling application must broadcast the <a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a> message to avoid causing instabilities in other applications.</div><div> </div>

## -parameters

### -param Locale [in]

For the ANSI version of the function, the <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a> of the locale with the code page used when interpreting the <i>lpLCData</i> information. For the Unicode version, this parameter is ignored.

You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

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
The following custom locale identifiers are also supported.

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

### -param LCType [in]

Type of locale information to set. For valid constants see "Constants Used in the LCType Parameter of GetLocaleInfo, GetLocaleInfoEx, and SetLocaleInfo" section of <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>. The application can specify only one value per call, but it can use the binary OR operator to combine <a href="/windows/desktop/Intl/locale-use-cp-acp">LOCALE_USE_CP_ACP</a> with any other constant.

### -param lpLCData [in]

Pointer to a null-terminated string containing the locale information to set. The information must be in the format specific to the specified constant. The application uses a Unicode string for the Unicode version of the function, and an ANSI string for the ANSI version.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_ACCESS_DISABLED_BY_POLICY. The group policy of the computer or the user has forbidden this operation.</li>
<li>ERROR_INVALID_ACCESS. The access code was invalid.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function writes to the registry, where it sets values that are associated with a particular user instead of a particular application. These registry values affect the behavior of other applications run by the user. As a rule, an application should call this function only when the user has explicitly requested the changes. The registry settings should not be changed for the convenience of a single application.

For the <i>LCType</i> parameter, the application should set <a href="/windows/desktop/Intl/locale-use-cp-acp">LOCALE_USE_CP_ACP</a> to use the operating system ANSI code page instead of the locale code page for string translation.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 

As of Windows Vista, the <a href="/windows/desktop/Intl/locale-sdate">LOCALE_SDATE</a> and <a href="/windows/desktop/Intl/locale-stime-constants">LOCALE_STIME</a> constants are obsolete. Do not use these constants. Use <a href="/windows/desktop/Intl/locale-sshortdate">LOCALE_SSHORTDATE</a> and <a href="/windows/desktop/Intl/locale-stime-constants">LOCALE_STIMEFORMAT</a> instead. A custom locale might not have a single, uniform separator character within the date or time format: for example, a format such as "12/31, 2006" or "03:56'23" might be valid.





> [!NOTE]
> The winnls.h header defines SetLocaleInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoa">GetLocaleInfo</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>

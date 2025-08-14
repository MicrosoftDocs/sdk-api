---
UID: NF:winnls.LCIDToLocaleName
title: LCIDToLocaleName function (winnls.h)
description: Converts a locale identifier to a locale name.
helpviewer_keywords: ["LCIDToLocaleName","LCIDToLocaleName function [Internationalization for Windows Applications]","_win32_LCIDToLocaleName","intl.lcidtolocalename","winnls/LCIDToLocaleName"]
old-location: intl\lcidtolocalename.htm
tech.root: Intl
ms.assetid: 63233e3e-5b7c-43cb-9c62-88b0791c2647
ms.date: 12/05/2018
ms.keywords: LCIDToLocaleName, LCIDToLocaleName function [Internationalization for Windows Applications], _win32_LCIDToLocaleName, intl.lcidtolocalename, winnls/LCIDToLocaleName
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
 - LCIDToLocaleName
 - winnls/LCIDToLocaleName
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
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - LCIDToLocaleName
---

# LCIDToLocaleName function


## -description

Converts a <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a> to a <a href="/windows/desktop/Intl/locale-names">locale name</a>. <div class="alert"><b>Note</b>  For custom locales, including those created by Microsoft, your applications should prefer locale names over locale identifiers.</div>
<div> </div>

## -parameters

### -param Locale [in]

Locale identifier to translate. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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
<b>Windows Vista:</b> The following custom locale identifiers are also supported.

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

### -param lpName [out, optional]

Pointer to a buffer in which this function retrieves the locale name, or one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param cchName [in]

Size, in characters, of the locale name buffer. The maximum possible length of a locale name, including a terminating null character, is <a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_MAX_LENGTH</a>. This is the recommended size to supply for this parameter.

Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the locale name buffer.

### -param dwFlags [in]

<b>Before Windows 7:</b> Reserved; should always be 0.

<b>Starting with Windows 7:</b> Can be set to <a href="/windows/desktop/Intl/locale-allow-neutral-names">LOCALE_ALLOW_NEUTRAL_NAMES</a> to allow the return of a neutral name.

## -returns

Returns the count of characters, including the terminating null character, in the locale name if successful. If the function succeeds and the value of <i>cchName</i> is 0, the return value is the required size, in characters (including nulls), for the locale name buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-localenametolcid">LocaleNameToLCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
---
UID: NF:winnls.ResolveLocaleName
title: ResolveLocaleName function (winnls.h)
description: Finds a possible locale name match for the supplied name.
helpviewer_keywords: ["ResolveLocaleName","ResolveLocaleName function [Internationalization for Windows Applications]","intl.resolvelocalename","winnls/ResolveLocaleName"]
old-location: intl\resolvelocalename.htm
tech.root: Intl
ms.assetid: 99264b22-3fb5-47e2-b0b9-42a6768e67c1
ms.date: 12/05/2018
ms.keywords: ResolveLocaleName, ResolveLocaleName function [Internationalization for Windows Applications], intl.resolvelocalename, winnls/ResolveLocaleName
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ResolveLocaleName
 - winnls/ResolveLocaleName
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
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - ResolveLocaleName
---

# ResolveLocaleName function


## -description

Finds a possible <a href="/windows/desktop/Intl/locale-names">locale name</a> match for the supplied name.

## -parameters

### -param lpNameToResolve [in, optional]

Pointer to a name to resolve, for example, "en-XA" for English (Private Use).

### -param lpLocaleName [out, optional]

Pointer to a buffer in which this function retrieves the locale name that is the match for the input name. For example, the match for the name "en-XA" is "en-US" for English (United States).

<div class="alert"><b>Note</b>  If the function fails, the state of the output buffer is not guaranteed to be accurate. In this case, the application should check the return value and error status set by the function to determine the correct course of action.</div>
<div> </div>

### -param cchLocaleName [in]

Size, in characters, of the buffer indicated by <i>lpLocaleName</i>. The maximum possible length of a locale name, including a terminating null character, is the value of <a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_MAX_LENGTH</a>. This is the recommended size to supply in this parameter.

## -returns

Returns the size of the buffer containing the locale name, including the terminating null character, if successful.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:
<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
</ul>

## -remarks

The retrieved locale name indicates a specific locale, including language and country/region, even if the input language is neutral. For example, an input of "en" for English (United States) causes the function to retrieve "en-US".

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application, nor does the return of a valid locale guarantee that it will be valid on another computer. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> Language tags obtained from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace must be converted by  <b>ResolveLocaleName</b> before they can be used with any National Language Support functions.

## -see-also

<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/uwp/api/Windows.Globalization">Windows.Globalization</a>
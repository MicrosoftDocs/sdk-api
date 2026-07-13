---
UID: NF:winnls.IsNormalizedString
title: IsNormalizedString function (winnls.h)
description: Verifies that a string is normalized according to Unicode 4.0 TR#15. For more information, see Using Unicode Normalization to Represent Strings.
helpviewer_keywords: ["IsNormalizedString","IsNormalizedString function [Internationalization for Windows Applications]","_win32_IsNormalizedString","intl.isnormalizedstring","winnls/IsNormalizedString"]
old-location: intl\isnormalizedstring.htm
tech.root: Intl
ms.assetid: 5a1d3977-9fe9-457f-b0a2-46b32bcc27db
ms.date: 12/05/2018
ms.keywords: IsNormalizedString, IsNormalizedString function [Internationalization for Windows Applications], _win32_IsNormalizedString, intl.isnormalizedstring, winnls/IsNormalizedString
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
req.lib: kernel32.Lib
req.dll: Normaliz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2 and later, orWindows Server 2003 with SP1
ms.custom: 19H1
f1_keywords:
 - IsNormalizedString
 - winnls/IsNormalizedString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Normaliz.dll
 - API-MS-Win-Core-normalization-l1-1-0.dll
 - KernelBase.dll
api_name:
 - IsNormalizedString
---

# IsNormalizedString function


## -description

Verifies that a string is normalized according to Unicode 4.0 TR#15. For more information, see <a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>.

## -parameters

### -param NormForm [in]

Normalization form to use. <a href="/windows/desktop/api/winnls/ne-winnls-norm_form">NORM_FORM</a> specifies the standard Unicode normalization forms.

### -param lpString [in]

Pointer to the string to test.

### -param cwLength [in]

Length, in characters, of the input string, including a null terminating character. If this value is -1, the function assumes the string to be null-terminated and calculates the length automatically.

## -returns

Returns <b>TRUE</b> if the input string is already normalized to the appropriate form, or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in string.</li>
<li>ERROR_SUCCESS. The action completed successfully but yielded no results.</li>
</ul>
If you need to reliably determine <b>FALSE</b> from an error condition, then it must call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>(ERROR_SUCCESS).

## -remarks

<b>Windows XP, Windows Server 2003</b>: 

No longer supported.

The required header file and DLL are part of the Microsoft Internationalized Domain Name (IDN) Mitigation APIs, which are no longer available for download.


#### Examples

An example showing the use of this function can be found in <a href="/windows/desktop/Intl/nls--unicode-normalization-sample">NLS: Unicode Normalization Sample</a>.



<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winnls/ne-winnls-norm_form">NORM_FORM</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-normalizestring">NormalizeString</a>



<a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>
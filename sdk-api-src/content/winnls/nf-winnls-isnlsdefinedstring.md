---
UID: NF:winnls.IsNLSDefinedString
title: IsNLSDefinedString function (winnls.h)
description: Determines if each character in a string has a defined result for a specified NLS capability.
helpviewer_keywords: ["IsNLSDefinedString","IsNLSDefinedString function [Internationalization for Windows Applications]","_win32_IsNLSDefinedString","intl.isnlsdefinedstring","winnls/IsNLSDefinedString"]
old-location: intl\isnlsdefinedstring.htm
tech.root: Intl
ms.assetid: 0beb0470-ecdc-4a24-b28c-0738e1df9d49
ms.date: 12/05/2018
ms.keywords: IsNLSDefinedString, IsNLSDefinedString function [Internationalization for Windows Applications], _win32_IsNLSDefinedString, intl.isnlsdefinedstring, winnls/IsNLSDefinedString
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
 - IsNLSDefinedString
 - winnls/IsNLSDefinedString
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
 - IsNLSDefinedString
---

# IsNLSDefinedString function


## -description

Determines if each character in a string has a defined result for a specified NLS capability.

## -parameters

### -param Function [in]

NLS capability to query. This value must be COMPARE_STRING. See the <a href="/windows/desktop/api/winnls/ne-winnls-sysnls_function">SYSNLS_FUNCTION</a> enumeration.

### -param dwFlags [in]

Flags defining the function. Must be 0.

### -param lpVersionInformation [in]

Pointer to an <a href="/windows/win32/api/winnls/ns-winnls-nlsversioninfo-r1">NLSVERSIONINFO</a> structure containing version information. Typically, the information is obtained by calling <a href="/windows/desktop/api/winnls/nf-winnls-getnlsversion">GetNLSVersion</a>. The application sets this parameter to <b>NULL</b> if the function is to use the current version.

### -param lpString [in]

Pointer to the UTF-16 string to examine.

### -param cchStr [in]

Number of UTF-16 characters in the string indicated by <i>lpString</i>. This count can include a terminating null character. If the terminating null character is included in the character count, it does not affect the checking behavior because the terminating null character is always defined.

The application should supply -1 to indicate that the string is null-terminated. In this case, the function itself calculates the string length.

## -returns

Returns <b>TRUE</b> if successful, only if the input string is valid, or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function differentiates between defined and undefined strings, so that an application such as Active Directory can reject strings with undefined code points. Use of the function can minimize the necessity for the application to re-index its database. For more information, see <a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>.

For example, if <i>Function</i> is set to COMPARE_STRING, <b>IsNLSDefinedString</b> checks for undefined code points, <a href="/windows/desktop/Intl/surrogates-and-supplementary-characters">surrogate pairs</a> that represent undefined Unicode characters, or ill-formed surrogate pairs. If the function returns <b>TRUE</b> for a particular string, the results, as retrieved by <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> or <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> with LCMAP_SORTKEY set, are guaranteed to be identical as long as the corresponding NLS version does not change.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getnlsversion">GetNLSVersion</a>



<a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>



<a href="/windows/win32/api/winnls/ns-winnls-nlsversioninfo-r1">NLSVERSIONINFO</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/ne-winnls-sysnls_function">SYSNLS_FUNCTION</a>
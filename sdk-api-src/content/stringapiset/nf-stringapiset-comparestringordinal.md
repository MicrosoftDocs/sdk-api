---
UID: NF:stringapiset.CompareStringOrdinal
title: CompareStringOrdinal function (stringapiset.h)
description: Compares two Unicode strings to test binary equivalence.
helpviewer_keywords: ["CompareStringOrdinal","CompareStringOrdinal function [Internationalization for Windows Applications]","_win32_CompareStringOrdinal","intl.comparestringordinal","stringapiset/CompareStringOrdinal"]
old-location: intl\comparestringordinal.htm
tech.root: Intl
ms.assetid: 6a457076-7992-4912-8ac5-2258f9651a8c
ms.date: 12/05/2018
ms.keywords: CompareStringOrdinal, CompareStringOrdinal function [Internationalization for Windows Applications], _win32_CompareStringOrdinal, intl.comparestringordinal, stringapiset/CompareStringOrdinal
req.header: stringapiset.h
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
 - CompareStringOrdinal
 - stringapiset/CompareStringOrdinal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-String-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CompareStringOrdinal
---

# CompareStringOrdinal function


## -description

Compares two <a href="/windows/desktop/Intl/unicode">Unicode</a> strings to test binary equivalence.

## -parameters

### -param lpString1 [in]

Pointer to the first string to compare.

### -param cchCount1 [in]

Length of the string indicated by <i>lpString1</i>. The application supplies -1 if the string is null-terminated. In this case, the function determines the length automatically.

### -param lpString2 [in]

Pointer to the second string to compare.

### -param cchCount2 [in]

Length of the string indicated by <i>lpString2</i>. The application supplies -1 if the string is null-terminated. In this case, the function determines the length automatically.

### -param bIgnoreCase [in]

<b>TRUE</b> if the function is to perform a case-insensitive comparison, using the operating system uppercase table information. The application sets this parameter to <b>FALSE</b> if the function is to compare the strings exactly as they are passed in. Note that 1 is the only numeric value that can be used to specify a true value for this boolean parameter that does not result an invalid parameter error. Boolean values for this parameter work as expected.

## -returns

Returns one of the following values if successful. To maintain the C runtime convention of comparing strings, the value 2 can be subtracted from a nonzero return value. Then, the meaning of &lt;0, ==0, and &gt;0 is consistent with the C runtime.

<ul>
<li>CSTR_LESS_THAN. The value indicated by <i>lpString1</i> is less than the value indicated by <i>lpString2</i>.</li>
<li>CSTR_EQUAL. The value indicated by <i>lpString1</i> equals the value indicated by <i>lpString2</i>.</li>
<li>CSTR_GREATER_THAN. The value indicated by <i>lpString1</i> is greater than the value indicated by <i>lpString2</i>.</li>
</ul>
The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:
<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function tests for binary equality, not linguistic equality. For information about the use of the function for ordinal sorting, see <a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>.

Applications that are concerned with linguistic equality should use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>, <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>, <a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpa">lstrcmp</a>, or <a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpia">lstrcmpi</a>. For more information about linguistic sorting, see <a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>


<b>Starting with Windows 8: </b><b>CompareStringOrdinal</b>  is declared in Stringapiset.h. Before Windows 8, it was declared in Winnls.h.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>



<a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>
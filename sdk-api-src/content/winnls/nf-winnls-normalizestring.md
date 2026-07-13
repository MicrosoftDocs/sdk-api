---
UID: NF:winnls.NormalizeString
title: NormalizeString function (winnls.h)
description: Normalizes characters of a text string according to Unicode 4.0 TR#15. For more information, see Using Unicode Normalization to Represent Strings.
helpviewer_keywords: ["NormalizeString","NormalizeString function [Internationalization for Windows Applications]","_win32_NormalizeString","intl.normalizestring","winnls/NormalizeString"]
old-location: intl\normalizestring.htm
tech.root: Intl
ms.assetid: ef76d0e5-2999-4a21-8522-c698013e3816
ms.date: 12/05/2018
ms.keywords: NormalizeString, NormalizeString function [Internationalization for Windows Applications], _win32_NormalizeString, intl.normalizestring, winnls/NormalizeString
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
 - NormalizeString
 - winnls/NormalizeString
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
 - NormalizeString
---

# NormalizeString function


## -description

Normalizes characters of a text string according to Unicode 4.0 TR#15. For more information, see <a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>.

## -parameters

### -param NormForm [in]

Normalization form to use. <a href="/windows/desktop/api/winnls/ne-winnls-norm_form">NORM_FORM</a> specifies the standard Unicode normalization forms.

### -param lpSrcString [in]

Pointer to the non-normalized source string.

### -param cwSrcLength [in]

Length, in characters, of the buffer containing the source string. The application can set this parameter to -1 if the function should assume the string to be null-terminated and calculate the length automatically.

### -param lpDstString [out, optional]

Pointer to a buffer in which the function retrieves the destination string. Alternatively, this parameter contains <b>NULL</b> if <i>cwDstLength</i> is set to 0.

<div class="alert"><b>Note</b>  The function does not null-terminate the string if the input string length is explicitly specified without a terminating null character. To null-terminate the output string, the application should specify -1 or explicitly count the terminating null character for the input string.</div>
<div> </div>

### -param cwDstLength [in]

Length, in characters, of the buffer containing the destination string. Alternatively, the application can set this parameter to 0 to request the function to return the required size for the destination buffer.

## -returns

Returns the length of the normalized string in the destination buffer. If <i>cwDstLength</i> is set to 0, the function returns the estimated buffer length required to do the actual conversion.

If the string in the input buffer is null-terminated or if <i>cwSrcLength</i> is -1, the string written to the destination buffer is null-terminated and the returned string length includes the terminating null character.

The function returns a value that is less than or equal to 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in a string. The return value is the negative of the index of the location of the error in the input string.</li>
<li>ERROR_SUCCESS. The action completed successfully but yielded no results.</li>
</ul>

## -remarks

Some Unicode characters have multiple equivalent binary representations consisting of sets of combining and/or composite Unicode characters. The Unicode standard defines a process called normalization that returns one binary representation when given any of the equivalent binary representations of a character. Normalization can be performed with several algorithms, called normalization forms, that obey different rules, as described in <a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>. The Win32 and the .NET Framework currently support normalization forms C, D, KC, and KD, as defined in <a href="https://www.unicode.org/reports/tr15">Unicode Standard Annex #15: Unicode Normalization Forms</a>. Normalized strings are typically evaluated with an ordinal comparison.

The following code demonstrates the use of the buffer length estimate:


```cpp
const int maxIterations = 10;
LPWSTR strResult = NULL;
HANDLE hHeap = GetProcessHeap();

int iSizeEstimated = NormalizeString(form, strInput, -1, NULL, 0);
for (int i = 0; i < maxIterations; i++)
{
    if (strResult)
        HeapFree(hHeap, 0, strResult);
    strResult = (LPWSTR)HeapAlloc(hHeap, 0, iSizeEstimated * sizeof (WCHAR));
    iSizeEstimated = NormalizeString(form, strInput, -1, strResult, iSizeEstimated);
 
    if (iSizeEstimated > 0)
        break; // success 
 
    if (iSizeEstimated <= 0)
    {
        DWORD dwError = GetLastError();
        if (dwError != ERROR_INSUFFICIENT_BUFFER) break; // Real error, not buffer error 
 
        // New guess is negative of the return value. 
        iSizeEstimated = -iSizeEstimated;
    }
}

```

<b>Windows XP, Windows Server 2003</b>: 

No longer supported.

The required header file and DLL are part of the Microsoft Internationalized Domain Name (IDN) Mitigation APIs, which are no longer available for download.


#### Examples

An example showing the use of this function can be found in <a href="/windows/desktop/Intl/nls--unicode-normalization-sample">NLS: Unicode Normalization Sample</a>.



<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-isnormalizedstring">IsNormalizedString</a>



<a href="/windows/desktop/api/winnls/ne-winnls-norm_form">NORM_FORM</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>
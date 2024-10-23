---
UID: NF:stringapiset.GetStringTypeExW
title: GetStringTypeExW function (stringapiset.h)
description: Retrieves character type information for the characters in the specified source string.
helpviewer_keywords: ["GetStringTypeEx","GetStringTypeEx function [Internationalization for Windows Applications]","GetStringTypeExA","GetStringTypeExW","_win32_GetStringTypeEx","_win32_GetStringTypeEx_cpp","intl.getstringtypeex","stringapiset/GetStringTypeEx","stringapiset/GetStringTypeExA","stringapiset/GetStringTypeExW","winui._win32_GetStringTypeEx"]
old-location: intl\getstringtypeex.htm
tech.root: Intl
ms.assetid: e0cd051f-6627-457a-9a83-d71de607f67f
ms.date: 10/23/2024
ms.keywords: GetStringTypeEx, GetStringTypeEx function [Internationalization for Windows Applications], GetStringTypeExA, GetStringTypeExW, _win32_GetStringTypeEx, _win32_GetStringTypeEx_cpp, intl.getstringtypeex, stringapiset/GetStringTypeEx, stringapiset/GetStringTypeExA, stringapiset/GetStringTypeExW, winui._win32_GetStringTypeEx
req.header: stringapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetStringTypeExW (Unicode) and GetStringTypeExA (ANSI)
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
 - GetStringTypeExW
 - stringapiset/GetStringTypeExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Deprecated-APIs-Legacy-l1-1-0.dll
 - API-MS-Win-Core-String-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Deprecated-APIs-Legacy-l1-2-0.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetStringTypeEx
 - GetStringTypeExA
 - GetStringTypeExW
---

# GetStringTypeExW function


## -description

> [!NOTE]
> This API may have incomplete/outdated information for certain Unicode characters, particularly those in the supplementary range. For more accurate and comprehensive Unicode character type information, consider using equivalent ICU APIs such as [u_charType](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/uchar_8h.html#a53f7567680cb6d92489d6e7750c90284), [u_islower](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/uchar_8h.html#a65980f5668ed1df7f183a090f62b0e61), [u_isspace](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/uchar_8h.html#a48dd198b451e691cf81eb41831474ddc), and [u_ispunct](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/uchar_8h.html#add0409f1e6cbbc84dda50c45cc3e7302). For guidance on using ICU APIs on Windows, see [Getting Started with ICU on Windows](/windows/win32/intl/international-components-for-unicode--icu-.md#getting-started).

Retrieves character type information for the characters in the specified source string. For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array. Each bit identifies a given character type, for example, letter, digit, or neither.
<div class="alert"><b>Caution</b>  Using the <b>GetStringTypeEx</b> function incorrectly can compromise the security of your application. To avoid a buffer overflow, the application must set the output buffer size correctly. For more security information, see <a href="/windows/desktop/AppUIStart/sec-ui">Security Considerations: Windows User Interface</a>.</div><div> </div><div class="alert"><b>Note</b>  Unlike its close relatives <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea">GetStringTypeA</a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a>, this function exhibits appropriate ANSI or Unicode behavior through the use of the #define UNICODE switch. This is the recommended function for character type retrieval.</div><div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. This value uniquely defines the ANSI code page. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

<ul>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
</ul>
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.


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

### -param dwInfoType [in]

Flags specifying the character type information to retrieve. For possible flag values, see the <i>dwInfoType</i> parameter of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a>. For detailed information about the character type bits, see Remarks for <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a>.

### -param lpSrcStr [in]

Pointer to the string for which to retrieve the character types. The string is assumed to be null-terminated if <i>cchSrc</i> is set to any negative value.

### -param cchSrc [in]

Size, in characters, of the string indicated by <i>lpSrcStr</i>. The size refers to bytes for the ANSI version of the function or wide characters for the Unicode version. If the size includes a terminating null character, the function retrieves character type information for that character. If the application sets the size to any negative integer, the source string is assumed to be null-terminated and the function calculates the size automatically with an additional character for the null termination.

### -param lpCharType [out]

Pointer to an array of 16-bit values. The length of this array must be large enough to receive one 16-bit value for each character in the source string. If <i>cchSrc</i> is not a negative number, <i>lpCharType</i> should be an array of words with <i>cchSrc</i> elements. If <i>cchSrc</i> is set to a negative number, <i>lpCharType</i> is an array of words with <i>lpSrcStr</i> + 1 elements. When the function returns, this array contains one word corresponding to each character in the source string.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li><b>ERROR_INVALID_FLAGS</b>. The values supplied for flags were not valid.</li>
<li><b>ERROR_INVALID_PARAMETER</b>. Any of the parameter values was invalid.</li>
</ul>

## -remarks

For an overview of the use of the string functions, see <a href="/windows/desktop/menurc/strings">Strings</a>.

Using the ANSI code page for the supplied locale, this function translates the source string from ANSI to Unicode. It then analyzes each Unicode character for character type information.

The ANSI version of this function converts the source string to Unicode and calls the 
corresponding <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a> function. Thus the words in the output buffer correspond not to the original ANSI string but to its Unicode equivalent. The conversion from ANSI to Unicode can result in a change in string length, for example, a pair of ANSI characters can map to a single 
Unicode character. Therefore, the correspondence between the words in the output buffer and the characters in the original ANSI string is not one-to-one in all cases, for example, multibyte strings. Thus, the ANSI version of this function is of limited use for multi-character strings. The Unicode version of the function is recommended instead.

This function circumvents a limitation caused by the difference in parameters between <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea">GetStringTypeA</a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a>. Because of the parameter difference, an application cannot automatically invoke the proper ANSI or Unicode version of a <b>GetStringType*</b> function through the use of the #define UNICODE switch. On the other hand, <b>GetStringTypeEx</b>, behaves properly with regard to that switch. Thus it is the recommended function.

    
When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 

The values of the <i>lpSrcStr</i> and <i>lpCharType</i> parameters must not be the same. If they are the same, the function fails with <b>ERROR_INVALID_PARAMETER</b>.

The <i>Locale</i> parameter is only used to perform string conversion to Unicode. It has nothing to do with the CTYPE* values supplied by the application. These values are solely determined by Unicode code points, and do not vary on a locale basis. For example, Greek letters are specified as C1_ALPHA for any value of <i>Locale</i>.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>

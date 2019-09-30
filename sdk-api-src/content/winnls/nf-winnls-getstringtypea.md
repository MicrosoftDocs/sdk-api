---
UID: NF:winnls.GetStringTypeA
title: GetStringTypeA function (winnls.h)
author: windows-sdk-content
description: Deprecated.
old-location: intl\getstringtypea.htm
tech.root: Intl
ms.assetid: 8fe771ae-80f6-473d-b2d8-8331c58ffb5a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStringTypeA, GetStringTypeA function [Internationalization for Windows Applications], _win32_GetStringTypeA, _win32_GetStringTypeA_cpp, intl.getstringtypea, winnls/GetStringTypeA, winui._win32_GetStringTypeA
ms.topic: function
f1_keywords: 
 - "winnls/GetStringTypeA"
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
 - GetStringTypeA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetStringTypeA function


## -description


Deprecated. Retrieves character type information for the characters in the specified source string. For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array. Each bit identifies a given character type, for example, letter, digit, or neither.      <div class="alert"><b>Caution</b>  Using the <b>GetStringTypeA</b> function incorrectly can compromise the security of your application. To avoid a buffer overflow, the application must set the output buffer size correctly. For more security information, see <a href="https://docs.microsoft.com/windows/desktop/AppUIStart/sec-ui">Security Considerations: Windows User Interface</a>.</div>
<div> </div>



## -parameters




### -param Locale [in]


<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. You can use the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
</ul>
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>

### -param dwInfoType [in]

Flags specifying the character type information to retrieve. For possible flag values, see the <i>dwInfoType</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a>. For detailed information about the character type bits, see Remarks for <a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a>.


### -param lpSrcStr [in]

Pointer to the ANSI string for which to retrieve the character types. The string can be a double-byte character set (DBCS) string if the supplied locale is appropriate for DBCS. The string is assumed to be null-terminated if <i>cchSrc</i> is set to any negative value.


### -param cchSrc [in]

Size, in characters, of the string indicated by <i>lpSrcStr</i>. If the size includes a terminating null character, the function retrieves character type information for that character. If the application sets the size to any negative integer, the source string is assumed to be null-terminated and the function calculates the size automatically with an additional character for the null termination.


### -param lpCharType [out]

Pointer to an array of 16-bit values. The length of this array must be large enough to receive one 16-bit value for each character in the source string. If <i>cchSrc</i> is not a negative number, <i>lpCharType</i> should be an array of words with <i>cchSrc</i> elements. If <i>cchSrc</i> is set to a negative number, <i>lpCharType</i> is an array of words with <i>lpSrcStr</i> + 1 elements. When the function returns, this array contains one word corresponding to each character in the source string.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



For an overview of the use of the string functions, see <a href="https://docs.microsoft.com/windows/desktop/menurc/strings">Strings</a>.

This function converts the source string to Unicode and calls the 
corresponding <a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a> function. Thus the words in the output buffer correspond not to the original ANSI string but to its Unicode equivalent. The conversion from ANSI to Unicode can result in a change in string length, for example, a pair of ANSI characters can map to a single 
Unicode character. Therefore, the correspondence between the words in the output buffer and the characters in the original ANSI string is not one-to-one in all cases, for example, multibyte strings. Thus <b>GetStringTypeA</b> is of limited use for multi-character strings. <a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getstringtypeexa">GetStringTypeEx</a> are recommended instead.

			 
When this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 

The values of the <i>lpSrcStr</i> and <i>lpCharType</i> parameters must not be the same. If they are the same, the function fails with ERROR_INVALID_PARAMETER.

The <i>Locale</i> parameter is only used to perform string conversion to Unicode. It has nothing to do with the CTYPE* values supplied by the application. These values are solely determined by Unicode code points, and do not vary on a locale basis. For example, Greek letters are specified as C1_ALPHA for any value of <i>Locale</i>.

The <i>Locale</i> parameter is not used by the corresponding <a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a> function. Because of the parameter difference, an application cannot automatically invoke the proper ANSI or Unicode version of a <b>GetStringType*</b> function through the use of the #define UNICODE switch. An application can circumvent this limitation by using <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getstringtypeexa">GetStringTypeEx</a>, which is the recommended function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-getstringtypeexa">GetStringTypeEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew">GetStringTypeW</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
 

 


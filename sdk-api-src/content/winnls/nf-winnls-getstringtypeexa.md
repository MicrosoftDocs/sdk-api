---
UID: NF:winnls.GetStringTypeExA
title: GetStringTypeExA function
author: windows-sdk-content
description: Retrieves character type information for the characters in the specified source string.
old-location: intl\getstringtypeex.htm
tech.root: Intl
ms.assetid: e0cd051f-6627-457a-9a83-d71de607f67f
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetStringTypeEx, GetStringTypeEx function [Internationalization for Windows Applications], GetStringTypeExA, GetStringTypeExW, _win32_GetStringTypeEx, _win32_GetStringTypeEx_cpp, intl.getstringtypeex, winnls/GetStringTypeEx, winnls/GetStringTypeExA, winnls/GetStringTypeExW, winui._win32_GetStringTypeEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnls.h
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetStringTypeExA function


## -description


Retrieves character type information for the characters in the specified source string. For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array. Each bit identifies a given character type, for example, letter, digit, or neither.
<div class="alert"><b>Caution</b>  Using the <b>GetStringTypeEx</b> function incorrectly can compromise the security of your application. To avoid a buffer overflow, the application must set the output buffer size correctly. For more security information, see <a href="sec_winui">Security Considerations: Windows User Interface</a>.</div><div> </div><div class="alert"><b>Note</b>  Unlike its close relatives <a href="https://msdn.microsoft.com/8fe771ae-80f6-473d-b2d8-8331c58ffb5a">GetStringTypeA</a> and <a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a>, this function exhibits appropriate ANSI or Unicode behavior through the use of the #define UNICODE switch. This is the recommended function for character type retrieval.</div><div> </div>

## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale. This value uniquely defines the ANSI code page. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

<ul>
<li>
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
</ul>
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.


<ul>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>



### -param dwInfoType [in]

Flags specifying the character type information to retrieve. For possible flag values, see the <i>dwInfoType</i> parameter of <a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a>. For detailed information about the character type bits, see Remarks for <a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a>.


### -param lpSrcStr [in]

Pointer to the string for which to retrieve the character types. The string is assumed to be null-terminated if <i>cchSrc</i> is set to any negative value.


### -param cchSrc [in]

Size, in characters, of the string indicated by <i>lpSrcStr</i>. The size refers to bytes for the ANSI version of the function or wide characters for the Unicode version. If the size includes a terminating null character, the function retrieves character type information for that character. If the application sets the size to any negative integer, the source string is assumed to be null-terminated and the function calculates the size automatically with an additional character for the null termination.


### -param lpCharType [out]

Pointer to an array of 16-bit values. The length of this array must be large enough to receive one 16-bit value for each character in the source string. If <i>cchSrc</i> is not a negative number, <i>lpCharType</i> should be an array of words with <i>cchSrc</i> elements. If <i>cchSrc</i> is set to a negative number, <i>lpCharType</i> is an array of words with <i>lpSrcStr</i> + 1 elements. When the function returns, this array contains one word corresponding to each character in the source string.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li><b>ERROR_INVALID_FLAGS</b>. The values supplied for flags were not valid.</li>
<li><b>ERROR_INVALID_PARAMETER</b>. Any of the parameter values was invalid.</li>
</ul>



## -remarks



For an overview of the use of the string functions, see <a href="_win32_strings_cpp">Strings</a>.

Using the ANSI code page for the supplied locale, this function translates the source string from ANSI to Unicode. It then analyzes each Unicode character for character type information.

The ANSI version of this function converts the source string to Unicode and calls the 
corresponding <a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a> function. Thus the words in the output buffer correspond not to the original ANSI string but to its Unicode equivalent. The conversion from ANSI to Unicode can result in a change in string length, for example, a pair of ANSI characters can map to a single 
Unicode character. Therefore, the correspondence between the words in the output buffer and the characters in the original ANSI string is not one-to-one in all cases, for example, multibyte strings. Thus, the ANSI version of this function is of limited use for multi-character strings. The Unicode version of the function is recommended instead.

This function circumvents a limitation caused by the difference in parameters between <a href="https://msdn.microsoft.com/8fe771ae-80f6-473d-b2d8-8331c58ffb5a">GetStringTypeA</a> and <a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a>. Because of the parameter difference, an application cannot automatically invoke the proper ANSI or Unicode version of a <b>GetStringType*</b> function through the use of the #define UNICODE switch. On the other hand, <b>GetStringTypeEx</b>, behaves properly with regard to that switch. Thus it is the recommended function.

    
When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 

The values of the <i>lpSrcStr</i> and <i>lpCharType</i> parameters must not be the same. If they are the same, the function fails with <b>ERROR_INVALID_PARAMETER</b>.

The <i>Locale</i> parameter is only used to perform string conversion to Unicode. It has nothing to do with the CTYPE* values supplied by the application. These values are solely determined by Unicode code points, and do not vary on a locale basis. For example, Greek letters are specified as C1_ALPHA for any value of <i>Locale</i>.




## -see-also




<a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 


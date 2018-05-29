---
UID: NF:winnls.GetStringTypeA
title: GetStringTypeA function
author: windows-sdk-content
description: Deprecated.
old-location: intl\getstringtypea.htm
old-project: Intl
ms.assetid: 8fe771ae-80f6-473d-b2d8-8331c58ffb5a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetStringTypeA, GetStringTypeA function [Internationalization for Windows Applications], _win32_GetStringTypeA, _win32_GetStringTypeA_cpp, intl.getstringtypea, winnls/GetStringTypeA, winui._win32_GetStringTypeA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: NORM_FORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
-	GetStringTypeA
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetStringTypeA function


## -description


Deprecated. Retrieves character type information for the characters in the specified source string. For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array. Each bit identifies a given character type, for example, letter, digit, or neither.      <div class="alert"><b>Caution</b>  Using the <b>GetStringTypeA</b> function incorrectly can compromise the security of your application. To avoid a buffer overflow, the application must set the output buffer size correctly. For more security information, see <a href="sec_winui">Security Considerations: Windows User Interface</a>.</div>
<div> </div>



## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

Pointer to the ANSI string for which to retrieve the character types. The string can be a double-byte character set (DBCS) string if the supplied locale is appropriate for DBCS. The string is assumed to be null-terminated if <i>cchSrc</i> is set to any negative value.


### -param cchSrc [in]

Size, in characters, of the string indicated by <i>lpSrcStr</i>. If the size includes a terminating null character, the function retrieves character type information for that character. If the application sets the size to any negative integer, the source string is assumed to be null-terminated and the function calculates the size automatically with an additional character for the null termination.


### -param lpCharType [out]

Pointer to an array of 16-bit values. The length of this array must be large enough to receive one 16-bit value for each character in the source string. If <i>cchSrc</i> is not a negative number, <i>lpCharType</i> should be an array of words with <i>cchSrc</i> elements. If <i>cchSrc</i> is set to a negative number, <i>lpCharType</i> is an array of words with <i>lpSrcStr</i> + 1 elements. When the function returns, this array contains one word corresponding to each character in the source string.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



For an overview of the use of the string functions, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>.

This function converts the source string to Unicode and calls the 
corresponding <a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a> function. Thus the words in the output buffer correspond not to the original ANSI string but to its Unicode equivalent. The conversion from ANSI to Unicode can result in a change in string length, for example, a pair of ANSI characters can map to a single 
Unicode character. Therefore, the correspondence between the words in the output buffer and the characters in the original ANSI string is not one-to-one in all cases, for example, multibyte strings. Thus <b>GetStringTypeA</b> is of limited use for multi-character strings. <a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a> and <a href="https://msdn.microsoft.com/e0cd051f-6627-457a-9a83-d71de607f67f">GetStringTypeEx</a> are recommended instead.

			 
When this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 

The values of the <i>lpSrcStr</i> and <i>lpCharType</i> parameters must not be the same. If they are the same, the function fails with ERROR_INVALID_PARAMETER.

The <i>Locale</i> parameter is only used to perform string conversion to Unicode. It has nothing to do with the CTYPE* values supplied by the application. These values are solely determined by Unicode code points, and do not vary on a locale basis. For example, Greek letters are specified as C1_ALPHA for any value of <i>Locale</i>.

The <i>Locale</i> parameter is not used by the corresponding <a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a> function. Because of the parameter difference, an application cannot automatically invoke the proper ANSI or Unicode version of a <b>GetStringType*</b> function through the use of the #define UNICODE switch. An application can circumvent this limitation by using <a href="https://msdn.microsoft.com/e0cd051f-6627-457a-9a83-d71de607f67f">GetStringTypeEx</a>, which is the recommended function.




## -see-also




<a href="https://msdn.microsoft.com/e0cd051f-6627-457a-9a83-d71de607f67f">GetStringTypeEx</a>



<a href="https://msdn.microsoft.com/092541ea-e568-4aa3-b99e-ce0bac9c120b">GetStringTypeW</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 


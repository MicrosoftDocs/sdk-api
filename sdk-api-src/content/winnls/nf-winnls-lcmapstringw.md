---
UID: NF:winnls.LCMapStringW
title: LCMapStringW function
author: windows-sdk-content
description: For a locale specified by identifier, maps one input character string to another using a specified transformation, or generates a sort key for the input string.
old-location: intl\lcmapstring.htm
old-project: Intl
ms.assetid: 84dda2cd-cbf9-45e9-b18c-7dea0b5bc991
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: LCMapString, LCMapString function [Internationalization for Windows Applications], LCMapStringA, LCMapStringW, _win32_LCMapString, intl.lcmapstring, winnls/LCMapString, winnls/LCMapStringA, winnls/LCMapStringW
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
req.unicode-ansi: LCMapStringW (Unicode) and LCMapStringA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - LCMapString
 - LCMapStringA
 - LCMapStringW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LCMapStringW function


## -description


For a locale specified by identifier, maps one input character string to another using a specified transformation, or generates a sort key for the input string. <div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/725e4e75-c328-40bc-a594-20a295a487c6">LCMapStringEx</a> function to <b>LCMapString</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. This recommendation applies especially to custom locales, including those created by Microsoft. Any application that will be run only on Windows Vista and later should use <a href="https://msdn.microsoft.com/725e4e75-c328-40bc-a594-20a295a487c6">LCMapStringEx</a>. </div>
<div> </div>



## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

<ul>
<li>
<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
</ul>
The following custom locale identifiers are also supported.

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

### -param dwMapFlags [in]

Flags specifying the type of transformation to use during string mapping or the type of sort key to generate. For detailed definitions, see the <i>dwMapFlags</i> parameter of <a href="https://msdn.microsoft.com/725e4e75-c328-40bc-a594-20a295a487c6">LCMapStringEx</a>.


### -param lpSrcStr [in]

Pointer to a source string that the function maps or uses for sort key generation. This string cannot have a size of 0.


### -param cchSrc [in]

Size, in characters, of the source string indicated by <i>lpSrcStr</i>. The size of the source string can include the terminating null character, but does not have to. If the terminating null character is included, the mapping behavior of the function is not greatly affected because the terminating null character is considered to be unsortable and always maps to itself.

The application can set the parameter to any negative value to specify that the source string is null-terminated. In this case, if <b>LCMapString</b> is being used in its string-mapping mode, the function calculates the string length itself, and null-terminates the mapped string indicated by <i>lpDestStr</i>.

The application cannot set this parameter to 0.


### -param lpDestStr [out, optional]

Pointer to a buffer in which this function retrieves the mapped string or a sort key. When the application uses this function to generate a sort key, the destination string can contain an odd number of bytes. The LCMAP_BYTEREV flag only reverses an even number of bytes. The last byte (odd-positioned) in the sort key is not reversed.

<div class="alert"><b>Note</b>  The destination string can be the same as the source string only if LCMAP_UPPERCASE or LCMAP_LOWERCASE is set. Otherwise, the strings cannot be the same. If they are, the function fails.</div>
<div> </div>
<div class="alert"><b>Note</b>  Upon failure of the function, the destination buffer might contain either partial results or no results at all. In this case, it is recommended for your application to consider any results invalid.</div>
<div> </div>

### -param cchDest [in]

Size, in characters, of the destination string indicated by <i>lpDestStr</i>. If the application is using the function for string mapping, it supplies a character count for this parameter. If space for a terminating null character is included in <i>cchSrc</i>, <i>cchDest</i> must also include space for a terminating null character.

If the application is using the function to generate a sort key, it supplies a byte count for the size. This byte count must include space for the sort key 0x00 terminator.

The application can set <i>cchDest</i> to 0. In this case, the function does not use the <i>lpDestStr</i> parameter and returns the required buffer size for the mapped string or sort key.


## -returns



Returns the number of characters or bytes in the translated string or sort key, including a terminating null character, if successful. If the function succeeds and the value of <i>cchDest</i> is 0, the return value is the size of the buffer required to hold the translated string or sort key, including a terminating null character.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



See Remarks for <a href="https://msdn.microsoft.com/725e4e75-c328-40bc-a594-20a295a487c6">LCMapStringEx</a>.

The ANSI version of <b>LCMapString</b> maps strings to and from Unicode based on the default Windows (ANSI) code page associated with the specified locale. When the ANSI version of this function is used with a Unicode-only locale, the function can succeed because the operating system uses the CP_ACP value, representing the system default Windows ANSI code page. However, characters that are undefined in the system code page appear in the string as a question mark (?).




## -see-also




<a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a>



<a href="https://msdn.microsoft.com/d65a67d1-a7e1-4d2a-ae8b-6b4ac7f2a987">FindNLSString</a>



<a href="https://msdn.microsoft.com/09bc53e1-69f4-4a71-82b3-1b1b84a1b84f">GetNLSVersion</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/725e4e75-c328-40bc-a594-20a295a487c6">LCMapStringEx</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 


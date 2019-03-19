---
UID: NF:winnls.CompareStringA
title: CompareStringA function (winnls.h)
author: windows-sdk-content
description: Compares two character strings, for a locale specified by identifier.Caution  Using CompareString incorrectly can compromise the security of your application.
old-location: intl\comparestring.htm
tech.root: Intl
ms.assetid: 4db84fa7-f3c2-48fb-ad7d-8673397c4b0e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CompareString, CompareString function [Internationalization for Windows Applications], CompareStringA, CompareStringW, _win32_CompareString, _win32_CompareString_cpp, intl.comparestring, stringapiset/CompareString, stringapiset/CompareStringA, stringapiset/CompareStringW, winnls/CompareString, winnls/CompareStringA, winnls/CompareStringW, winui._win32_CompareString
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CompareStringW (Unicode) and CompareStringA (ANSI)
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
 - API-MS-Win-Core-String-l1-1-0.dll
 - API-MS-Win-deprecated-apis-Obsolete-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
 - CompareString
 - CompareStringA
 - CompareStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CompareStringA function


## -description


Compares two character strings, for a <a href="https://msdn.microsoft.com/8214c00d-4ec6-4597-8088-7819a160f0dc">locale</a> specified by identifier.
<div class="alert"><b>Caution</b>  Using <b>CompareString</b> incorrectly can compromise the security of your application. Strings that are not compared correctly can produce invalid input. For example, the function can raise security issues when used for a non-linguistic comparison, because two strings that are distinct in their binary representation can be linguistically equivalent. The application should test strings for validity before using them, and should provide error handlers. For more information, see <a href="https://msdn.microsoft.com/4034f479-ad29-4c6f-82c6-977f420c4d4d">Security Considerations: International Features</a>.</div><div> </div><div class="alert"><b>Note</b>  For compatibility with Unicode, your applications should prefer <a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a> or the Unicode version of <b>CompareString</b>. Another reason for preferring <a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a> is that Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales, for interoperability reasons. Any application that will be run only on Windows Vista and later should use <a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a>.</div><div> </div>

## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> of the locale used for the comparison. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

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

### -param dwCmpFlags [in]

Flags that indicate how the function compares the two strings. For detailed definitions, see the <i>dwCmpFlags</i> parameter of <a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a>.


### -param lpString1 [in]

Pointer to the first string to compare.


### -param cchCount1 [in]

Length of the string indicated by <i>lpString1</i>, excluding the terminating null character. This value represents bytes for the ANSI version of the function and wide characters for the Unicode version. The application can supply a negative value if the string is null-terminated. In this case, the function determines the length automatically.


### -param lpString2 [in]

Pointer to the second string to compare.


### -param cchCount2 [in]

Length of the string indicated by <i>lpString2</i>, excluding the terminating null character. This value represents bytes for the ANSI version of the function and wide characters for the Unicode version. The application can supply a negative value if the string is null-terminated. In this case, the function determines the length automatically.


## -returns



Returns the values described for <a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a>.




## -remarks



See Remarks for <a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a>.

If your application is calling the ANSI version of <b>CompareString</b>, the function converts parameters via the default code page of the supplied locale. Thus, an application can never use <b>CompareString</b> to handle UTF-8 text.

Normally, for case-insensitive comparisons, <b>CompareString</b> maps the lowercase "i" to the uppercase "I", even when the locale is Turkish or Azerbaijani. The  NORM_LINGUISTIC_CASING flag overrides this behavior for Turkish or Azerbaijani. If this flag is specified in conjunction with Turkish or Azerbaijani, LATIN SMALL LETTER DOTLESS I (U+0131) is the lowercase form of LATIN CAPITAL LETTER I (U+0049) and LATIN SMALL LETTER I (U+0069) is the lowercase form of LATIN CAPITAL LETTER I WITH DOT ABOVE (U+0130).

<b>Starting with Windows 8: </b>The ANSI version of the function is declared in Winnls.h, and the Unicode version is declared in Stringapiset.h. Before Windows 8, both versions were declared in Winnls.h.




## -see-also




<a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/4034f479-ad29-4c6f-82c6-977f420c4d4d">Security Considerations: International Features</a>



<a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>
 

 


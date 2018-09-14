---
UID: NF:winnls.IsNLSDefinedString
title: IsNLSDefinedString function
author: windows-sdk-content
description: Determines if each character in a string has a defined result for a specified NLS capability.
old-location: intl\isnlsdefinedstring.htm
tech.root: Intl
ms.assetid: 0beb0470-ecdc-4a24-b28c-0738e1df9d49
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IsNLSDefinedString, IsNLSDefinedString function [Internationalization for Windows Applications], _win32_IsNLSDefinedString, intl.isnlsdefinedstring, winnls/IsNLSDefinedString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - IsNLSDefinedString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsNLSDefinedString function


## -description


Determines if each character in a string has a defined result for a specified NLS capability.


## -parameters




### -param Function [in]

NLS capability to query. This value must be COMPARE_STRING. See the <a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a> enumeration.


### -param dwFlags [in]

Flags defining the function. Must be 0.


### -param lpVersionInformation [in]

Pointer to an <a href="https://msdn.microsoft.com/6afc8972-373c-4198-ac54-c2a6172b3b39">NLSVERSIONINFO</a> structure containing version information. Typically, the information is obtained by calling <a href="https://msdn.microsoft.com/09bc53e1-69f4-4a71-82b3-1b1b84a1b84f">GetNLSVersion</a>. The application sets this parameter to <b>NULL</b> if the function is to use the current version. 


### -param lpString [in]

Pointer to the UTF-16 string to examine.


### -param cchStr [in]

Number of UTF-16 characters in the string indicated by <i>lpString</i>. This count can include a terminating null character. If the terminating null character is included in the character count, it does not affect the checking behavior because the terminating null character is always defined.

The application should supply -1 to indicate that the string is null-terminated. In this case, the function itself calculates the string length.


## -returns



Returns <b>TRUE</b> if successful, only if the input string is valid, or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function differentiates between defined and undefined strings, so that an application such as Active Directory can reject strings with undefined code points. Use of the function can minimize the necessity for the application to re-index its database. For more information, see <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>.

For example, if <i>Function</i> is set to COMPARE_STRING, <b>IsNLSDefinedString</b> checks for undefined code points, <a href="https://msdn.microsoft.com/0dea39e2-a2b4-47fc-b44a-56af8ba1e346">surrogate pairs</a> that represent undefined Unicode characters, or ill-formed surrogate pairs. If the function returns <b>TRUE</b> for a particular string, the results, as retrieved by <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> or <a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapString</a> with LCMAP_SORTKEY set, are guaranteed to be identical as long as the corresponding NLS version does not change.




## -see-also




<a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a>



<a href="https://msdn.microsoft.com/09bc53e1-69f4-4a71-82b3-1b1b84a1b84f">GetNLSVersion</a>



<a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapString</a>



<a href="https://msdn.microsoft.com/6afc8972-373c-4198-ac54-c2a6172b3b39">NLSVERSIONINFO</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a>
 

 


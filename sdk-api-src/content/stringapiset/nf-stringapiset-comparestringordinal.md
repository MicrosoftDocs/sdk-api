---
UID: NF:stringapiset.CompareStringOrdinal
title: CompareStringOrdinal function
author: windows-sdk-content
description: Compares two Unicode strings to test binary equivalence.
old-location: intl\comparestringordinal.htm
old-project: Intl
ms.assetid: 6a457076-7992-4912-8ac5-2258f9651a8c
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: CompareStringOrdinal, CompareStringOrdinal function [Internationalization for Windows Applications], _win32_CompareStringOrdinal, intl.comparestringordinal, stringapiset/CompareStringOrdinal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MPR50_SERVICE_CHARACTERISTICS
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# CompareStringOrdinal function


## -description


Compares two <a href="https://msdn.microsoft.com/ca5bcdee-ea13-4745-a565-5426c462892d">Unicode</a> strings to test binary equivalence.


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

<b>TRUE</b> if the function is to perform a case-insensitive comparison, using the operating system uppercase table information. The application sets this parameter to <b>FALSE</b> if the function is to compare the strings exactly as they are passed in.


## -returns



Returns one of the following values if successful. To maintain the C runtime convention of comparing strings, the value 2 can be subtracted from a nonzero return value. Then, the meaning of &lt;0, ==0, and &gt;0 is consistent with the C runtime.

<ul>
<li>CSTR_LESS_THAN. The value indicated by <i>lpString1</i> is less than the value indicated by <i>lpString2</i>.</li>
<li>CSTR_EQUAL. The value indicated by <i>lpString1</i> equals the value indicated by <i>lpString2</i>.</li>
<li>CSTR_GREATER_THAN. The value indicated by <i>lpString1</i> is greater than the value indicated by <i>lpString2</i>.</li>
</ul>
The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:
<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>





## -remarks



This function tests for binary equality, not linguistic equality. For information about the use of the function for ordinal sorting, see <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>.

Applications that are concerned with linguistic equality should use <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a>, <a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a>, <a href="_win32_lstrcmp_cpp">lstrcmp</a>, or <a href="_win32_lstrcmpi_cpp">lstrcmpi</a>. For more information about linguistic sorting, see <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>


<b>Starting with Windows 8: </b><b>CompareStringOrdinal</b>  is declared in Stringapiset.h. Before Windows 8, it was declared in Winnls.h.




## -see-also




<a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a>



<a href="https://msdn.microsoft.com/264c67b6-848d-48ef-9bfa-4990bfa2fbf5">CompareStringEx</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/4034f479-ad29-4c6f-82c6-977f420c4d4d">Security Considerations: International Features</a>



<a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>
 

 


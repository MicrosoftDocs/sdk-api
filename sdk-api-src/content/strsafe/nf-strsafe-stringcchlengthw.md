---
UID: NF:strsafe.StringCchLengthW
title: StringCchLengthW function
author: windows-sdk-content
description: Determines whether a string exceeds the specified length, in characters.
old-location: menurc\stringcchlength.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcchlength.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: StringCchLength, StringCchLength function [Menus and Other Resources], StringCchLengthA, StringCchLengthW, UnalignedStringCchLength, _shell_StringCchLength, _shell_stringcchlength_cpp, menurc.stringcchlength, strsafe/StringCchLength, strsafe/StringCchLengthA, strsafe/StringCchLengthW, winui._shell_stringcchlength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchLengthW (Unicode) and StringCchLengthA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strsafe.h
api_name:
 - StringCchLength
 - StringCchLengthA
 - StringCchLengthW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StringCchLengthW function


## -description


Determines whether a  string exceeds the specified length, in characters.

<b>StringCchLength</b> is a replacement for the following functions:
<ul>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=192495">strlen, wcslen, _tcslen</a></li>
</ul>

## -parameters




### -param psz [in]

Type: <b>LPCTSTR</b>

The string whose length is to be checked.


### -param cchMax [in]

Type: <b>size_t</b>

The maximum number of characters allowed in <i>psz</i>, including the terminating null character. This value cannot exceed <b>STRSAFE_MAX_CCH</b>.


### -param pcchLength [out]

Type: <b>size_t*</b>

The number of characters in <i>psz</i>, not including the terminating null character. This value is valid only if <i>pcch</i> is not <b>NULL</b> and the function succeeds.


## -returns



Type: <b>HRESULT</b>

This function can return one of the following values. It is strongly recommended that you use the <a href="https://msdn.microsoft.com/7a258b0b-d214-46c5-be0a-6493cd14a0e5">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/d9c4ff73-c255-4a82-b901-23bd5b41ee6c">FAILED</a> macros to test the return value of this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The string at <i>psz</i> was not <b>NULL</b>, and the length of the string (including the terminating null character) is less than or equal to <i>cchMax</i> characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>psz</i> is <b>NULL</b>, <i>cchMax</i> is larger than <b>STRSAFE_MAX_CCH</b>, or <i>psz</i> is longer than <i>cchMax</i>.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.




## -remarks



Compared to  the functions it replaces, <b>StringCchLength</b> is an additional tool for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns.

<b>StringCchLength</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCchLengthA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCchLength</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCchLengthW</b></td>
</tr>
</table>
 


<a href="https://msdn.microsoft.com/35571305-9ef4-4215-ad88-80590e9b89cc">UnalignedStringCchLength</a> is an alias for this function.




## -see-also




<a href="https://msdn.microsoft.com/a1aa834c-53e7-4321-9db4-86f32ef31dc4">StringCbLength</a>
 

 


---
UID: NF:strsafe.StringCbLengthA
title: StringCbLengthA function
author: windows-sdk-content
description: Determines whether a string exceeds the specified length, in bytes.
old-location: menurc\stringcblength.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcblength.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: StringCbLength, StringCbLength function [Menus and Other Resources], StringCbLengthA, StringCbLengthW, UnalignedStringCbLength, _shell_StringCbLength, _shell_stringcblength_cpp, menurc.stringcblength, strsafe/StringCbLength, strsafe/StringCbLengthA, strsafe/StringCbLengthW, winui._shell_stringcblength
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
req.unicode-ansi: StringCbLengthW (Unicode) and StringCbLengthA (ANSI)
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
 - StringCbLength
 - StringCbLengthA
 - StringCbLengthW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- StringCbLengthA
: 
---

# StringCbLengthA function


## -description


Determines whether a  string exceeds the specified length, in bytes.

<b>StringCbLength</b> is a replacement for the following functions:
<ul>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=192495">strlen, wcslen, _tcslen</a></li>
</ul>

## -parameters




### -param psz [in]

Type: <b>LPCTSTR</b>

The string whose length is to be checked.


### -param cbMax [in]

Type: <b>size_t</b>

The maximum number of bytes allowed in <i>psz</i>, including those used for the terminating null character. This value cannot exceed <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.


### -param pcbLength [out]

Type: <b>size_t*</b>

The number of bytes in <i>psz</i>, excluding those used for the terminating null character. This value is valid only if <i>pcb</i> is not <b>NULL</b> and the function succeeds.


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
The string at <i>psz</i> was not <b>NULL</b>, and the length of the string (including the terminating null character) is less than or equal to <i>cbMax</i> characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>psz</i> is <b>NULL</b>, <i>cbMax</i> is larger than <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>, or <i>psz</i> is longer than <i>cbMax</i>.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.




## -remarks



Compared to  the functions it replaces, <b>StringCbLength</b> is an additional tool for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns.

<b>StringCbLength</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCbLengthA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCbLength</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCbLengthW</b></td>
</tr>
</table>
 


<a href="https://msdn.microsoft.com/2aa104f8-44e2-4896-86d8-5e2b6d9d7b73">UnalignedStringCbLength</a> is an alias for this function.




## -see-also




<a href="https://msdn.microsoft.com/4b29469a-e9a8-4309-9d19-db74a8bd6038">StringCchLength</a>
 

 


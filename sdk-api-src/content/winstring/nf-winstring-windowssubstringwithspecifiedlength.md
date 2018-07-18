---
UID: NF:winstring.WindowsSubstringWithSpecifiedLength
title: WindowsSubstringWithSpecifiedLength function
author: windows-sdk-content
description: Retrieves a substring from the specified string. The substring starts at a specified character position and has a specified length.
old-location: winrt\windowssubstringwithspecifiedlength.htm
old-project: WinRT
ms.assetid: 8E5DA806-8CBA-4569-9A9B-3B30350F603D
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: WindowsSubstringWithSpecifiedLength, WindowsSubstringWithSpecifiedLength function [Windows Runtime], winrt.windowssubstringwithspecifiedlength, winstring/WindowsSubstringWithSpecifiedLength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winstring.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - winstring.h
 - API-MS-Win-Core-WinRT-String-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
 - WindowsSubstringWithSpecifiedLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WindowsSubstringWithSpecifiedLength function


## -description


Retrieves a substring from the specified string. The substring starts at a specified character position and has a specified length.


## -parameters




### -param string [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The original string.


### -param startIndex [in]

Type: <b>UINT32</b>

The zero-based starting character position of a substring in this instance.


### -param length [in]

Type: <b>UINT32</b>

The number of characters in the substring.


### -param newString [out]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>*</b>

A string that is equivalent to the substring that begins at <i>startIndex</i> in <i>string</i>, or <b>NULL</b> if <i>startIndex</i> is equal to the length of <i>string</i>.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

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
The  substring was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>newString</i> is <b>NULL</b>, or <i>startIndex</i> plus <i>length</i> is greater than <b>MAXUINT32</b>, which is  4,294,967,295; that is, hexadecimal 0xFFFFFFFF.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
<i>startIndex</i> is greater than the length of <i>string</i>, or <i>startIndex</i> plus <i>length</i> indicates a position not within  <i>string</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the new substring.

</td>
</tr>
</table>
 




## -remarks



Each call to the <b>WindowsSubstringWithSpecifiedLength</b> function must be matched with a corresponding call to <a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>.




## -see-also




<a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>
 

 


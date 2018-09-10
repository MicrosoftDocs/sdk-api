---
UID: NF:winstring.WindowsReplaceString
title: WindowsReplaceString function
author: windows-sdk-content
description: Replaces all occurrences of a set of characters in the specified string with another set of characters to create a new string.
old-location: winrt\windowsreplacestring.htm
tech.root: WinRT
ms.assetid: 9675A3EA-12F9-4EE9-93D1-1138FEEB7CA4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WindowsReplaceString, WindowsReplaceString function [Windows Runtime], winrt.windowsreplacestring, winstring/WindowsReplaceString
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
 - WindowsReplaceString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WindowsReplaceString function


## -description


Replaces all occurrences of a set of characters in the specified string with another set of characters to create a new string.


## -parameters




### -param string [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The original string.


### -param stringReplaced [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The string to be replaced.


### -param stringReplaceWith [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The string to replace all occurrences of <i>stringReplaced</i>. 
If this parameter is <b>NULL</b>, all instances of <i>stringReplaced</i> are removed.


### -param newString [out]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>*</b>

A string that is equivalent to the original, except that all instances of <i>stringReplaced</i> are replaced with <i>stringReplaceWith</i>.


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
The  string replacement was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>newString</i> is <b>NULL</b>, <i>stringReplaced</i> is empty, or the length of <i>string1</i> plus the length of <i>string2</i> is greater than <b>MAXUINT32</b>, which is  4,294,967,295; that is, hexadecimal 0xFFFFFFFF. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the new string.

</td>
</tr>
</table>
 




## -remarks



Each call to the <b>WindowsReplaceString</b> function must be matched with a corresponding call to <a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>.




## -see-also




<a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>
 

 


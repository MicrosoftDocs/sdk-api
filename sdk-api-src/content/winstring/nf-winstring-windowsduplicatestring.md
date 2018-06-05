---
UID: NF:winstring.WindowsDuplicateString
title: WindowsDuplicateString function
author: windows-sdk-content
description: Creates a copy of the specified string.
old-location: winrt\windowsduplicatestring.htm
old-project: WinRT
ms.assetid: 65343F8A-ACD5-4BD2-83CD-DA9F71690DF3
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: WindowsDuplicateString, WindowsDuplicateString function [Windows Runtime], winrt.windowsduplicatestring, winstring/WindowsDuplicateString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winstring.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	winstring.h
-	API-MS-Win-Core-WinRT-String-l1-1-0.dll
-	ComBase.dll
-	API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
-	WindowsDuplicateString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WindowsDuplicateString function


## -description


Creates a copy of the specified string.


## -parameters




### -param string [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The string to be copied.


### -param newString [out]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>*</b>

A copy of <i>string</i>.


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
The  <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> was copied successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>newString</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the new <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>.

</td>
</tr>
</table>
 




## -remarks



Use the <b>WindowsDuplicateString</b>  function to copy an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>. If <i>string</i> was created by calling the <a href="https://msdn.microsoft.com/CACEFB80-A47E-45A7-9E13-29C1326B9453">WindowsCreateString</a> function, the reference count of the backing buffer is incremented. If <i>string</i> was created by calling the <a href="https://msdn.microsoft.com/0361BB7E-DA49-4289-A93E-DE7AAB8712AC">WindowsCreateStringReference</a> function,  the Windows Runtime copies its source string to a new buffer and starts a reference count, which means that  <i>newString</i> is not a fast-pass string. 

Each call to the <b>WindowsDuplicateString</b> function must be matched with a corresponding call to <a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>.




## -see-also




<a href="https://msdn.microsoft.com/CACEFB80-A47E-45A7-9E13-29C1326B9453">WindowsCreateString</a>



<a href="https://msdn.microsoft.com/0361BB7E-DA49-4289-A93E-DE7AAB8712AC">WindowsCreateStringReference</a>



<a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>
 

 


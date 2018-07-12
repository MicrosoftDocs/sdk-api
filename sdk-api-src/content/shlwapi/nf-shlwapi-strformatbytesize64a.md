---
UID: NF:shlwapi.StrFormatByteSize64A
title: StrFormatByteSize64A function
author: windows-sdk-content
description: Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.
old-location: shell\StrFormatByteSize64A.htm
old-project: shell
ms.assetid: b56dd90a-7033-409b-a8ea-e81a7a8a2342
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: StrFormatByteSize64, StrFormatByteSize64 function [Windows Shell], StrFormatByteSize64A, _win32_StrFormatByteSize64A, shell.StrFormatByteSize64A, shlwapi/StrFormatByteSize64, shlwapi/StrFormatByteSize64A
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrFormatByteSize64A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StrFormatByteSize64
 - StrFormatByteSize64A
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrFormatByteSize64A function


## -description


Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.


## -parameters




### -param qdw

Type: <b>LONGLONG</b>

The numeric value to be converted.


### -param pszBuf [out]

Type: <b>PSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the converted number.


### -param cchBuf

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszBuf</i>, in characters.


## -returns



Type: <b>PSTR</b>

Returns a pointer to the converted string, or <b>NULL</b> if the conversion fails.




## -remarks



<b>StrFormatByteSize64</b> can be used for either ANSI or Unicode characters. However, while <b>StrFormatByteSize64A</b> can be called directly, <b>StrFormatByteSize64W</b> is not defined. When <b>StrFormatByteSize64</b> is called with a Unicode value, <a href="https://msdn.microsoft.com/00192755-9135-4193-90bc-6e312b294007">StrFormatByteSizeW</a> is used.

In Windows 10, size is reported in base 10 rather than  base 2. For example, 1 KB is 1000 bytes rather than 1024.

The following table illustrates how this function converts a numeric value into a text string.

<table class="clsStd">
<tr>
<th>Numeric value</th>
<th>Text string</th>
</tr>
<tr>
<td>532</td>
<td>532 bytes</td>
</tr>
<tr>
<td>1340</td>
<td>1.30 KB</td>
</tr>
<tr>
<td>23506</td>
<td>23.5 KB</td>
</tr>
<tr>
<td>2400016</td>
<td>2.40 MB</td>
</tr>
<tr>
<td>2400000000</td>
<td>2.4 GB</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/244f93cb-0976-4a31-958c-ae0ed81c1dcf">StrFormatByteSizeA</a>



<a href="https://msdn.microsoft.com/00192755-9135-4193-90bc-6e312b294007">StrFormatByteSizeW</a>
 

 


---
UID: NF:shlwapi.StrFormatByteSizeA
title: StrFormatByteSizeA function (shlwapi.h)
description: Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size. Differs from StrFormatByteSizeW in one parameter type.
helpviewer_keywords: ["StrFormatByteSizeA", "StrFormatByteSizeA function [Windows Shell]", "_win32_StrFormatByteSizeA", "shell.StrFormatByteSizeA", "shlwapi/StrFormatByteSizeA"]
old-location: shell\StrFormatByteSizeA.htm
tech.root: shell
ms.assetid: 244f93cb-0976-4a31-958c-ae0ed81c1dcf
ms.date: 12/05/2018
ms.keywords: StrFormatByteSizeA, StrFormatByteSizeA function [Windows Shell], _win32_StrFormatByteSizeA, shell.StrFormatByteSizeA, shlwapi/StrFormatByteSizeA
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrFormatByteSizeA
 - shlwapi/StrFormatByteSizeA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StrFormatByteSizeA
---

# StrFormatByteSizeA function


## -description

Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size. Differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesizew">StrFormatByteSizeW</a> in one parameter type.

## -parameters

### -param dw

Type: <b>DWORD</b>

The numeric value to be converted.

### -param pszBuf [out]

Type: <b>PSTR</b>

A pointer to a buffer that receives the converted string.

### -param cchBuf

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszBuf</i>, in characters.

## -returns

Type: <b>PSTR</b>

Returns a pointer to the converted string, or <b>NULL</b> if the conversion fails.

## -remarks

The first parameter of this function has a different type for the ANSI and Unicode versions. If your numeric value is a <b>DWORD</b>, you can use <b>StrFormatByteSize</b> with text macros for both cases. The compiler will cast the numerical value to a <b>LONGLONG</b> for the Unicode case. If your numerical value is a <b>LONGLONG</b>, you should use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesizew">StrFormatByteSizeW</a> explicitly.

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
<td>22.9 KB</td>
</tr>
<tr>
<td>2400016</td>
<td>2.28 MB</td>
</tr>
<tr>
<td>2400000000</td>
<td>2.23 GB</td>
</tr>
</table>
 





> [!NOTE]
> The shlwapi.h header defines StrFormatByteSize as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesize64a">StrFormatByteSize64</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesizeex">StrFormatByteSizeEx</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesizew">StrFormatByteSizeW</a>

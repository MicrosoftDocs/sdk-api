---
UID: NF:shlwapi.StrFormatByteSizeEx
title: StrFormatByteSizeEx function (shlwapi.h)
description: Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size.
helpviewer_keywords: ["StrFormatByteSizeEx","StrFormatByteSizeEx function [Windows Shell]","_win32_StrFormatByteSizeEx","shell.StrFormatByteSizeEx","shlwapi/StrFormatByteSizeEx"]
old-location: shell\StrFormatByteSizeEx.htm
tech.root: shell
ms.assetid: 9ecc6427-e7bb-43ec-ab78-665ef52f8b10
ms.date: 12/05/2018
ms.keywords: StrFormatByteSizeEx, StrFormatByteSizeEx function [Windows Shell], _win32_StrFormatByteSizeEx, shell.StrFormatByteSizeEx, shlwapi/StrFormatByteSizeEx
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrFormatByteSizeEx
 - shlwapi/StrFormatByteSizeEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - StrFormatByteSizeEx
---

# StrFormatByteSizeEx function


## -description

Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size. Extends <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesizew">StrFormatByteSizeW</a> by offering the option to round to the nearest displayed digit or to discard undisplayed digits.

## -parameters

### -param ull

Type: <b>ULONGLONG</b>

The numeric value to be converted.

### -param flags

Type: <b><a href="/windows/win32/api/shlwapi/ne-shlwapi-tagsfbs_flags">SFBS_FLAGS</a></b>

One of the <a href="/windows/win32/api/shlwapi/ne-shlwapi-tagsfbs_flags">SFBS_FLAGS</a> enumeration values that specifies whether to round or truncate undisplayed digits. This value cannot be NULL.

### -param pszBuf [out]

Type: <b>PWSTR</b>

A pointer to a buffer that receives the converted string.

### -param cchBuf

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszBuf</i>, in characters.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following table illustrates how this function converts a numeric value into a text string in relation to the passed flag.

<table class="clsStd">
<tr>
<th>Numeric value</th>
<th>Flag</th>
<th>Text string</th>
</tr>
<tr>
<td>2147483647</td>
<td>SFBS_FLAGS_ROUND_TO_NEAREST_DISPLAYED_DIGIT</td>
<td>2.00 GB</td>
</tr>
<tr>
<td>2147483647</td>
<td>SFBS_FLAGS_TRUNCATE_UNDISPLAYED_DECIMAL_DIGITS</td>
<td>1.99 GB</td>
</tr>
</table>
 

In Windows 10, size is reported in base 10 rather than  base 2. For example, 1 KB is 1000 bytes rather than 1024.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesize64a">StrFormatByteSize64</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesizea">StrFormatByteSizeA</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strformatbytesizew">StrFormatByteSizeW</a>
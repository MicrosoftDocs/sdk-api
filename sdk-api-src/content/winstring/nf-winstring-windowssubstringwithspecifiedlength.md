---
UID: NF:winstring.WindowsSubstringWithSpecifiedLength
title: WindowsSubstringWithSpecifiedLength function (winstring.h)
description: Retrieves a substring from the specified string. The substring starts at a specified character position and has a specified length.
helpviewer_keywords: ["WindowsSubstringWithSpecifiedLength","WindowsSubstringWithSpecifiedLength function [Windows Runtime]","winrt.windowssubstringwithspecifiedlength","winstring/WindowsSubstringWithSpecifiedLength"]
old-location: winrt\windowssubstringwithspecifiedlength.htm
tech.root: WinRT
ms.assetid: 8E5DA806-8CBA-4569-9A9B-3B30350F603D
ms.date: 12/05/2018
ms.keywords: WindowsSubstringWithSpecifiedLength, WindowsSubstringWithSpecifiedLength function [Windows Runtime], winrt.windowssubstringwithspecifiedlength, winstring/WindowsSubstringWithSpecifiedLength
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WindowsSubstringWithSpecifiedLength
 - winstring/WindowsSubstringWithSpecifiedLength
dev_langs:
 - c++
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
---

## -description

Retrieves a substring from the specified string. The substring starts at a specified character position and has a specified length.

## -parameters

### -param string

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The original string.

### -param startIndex

Type: [in] <b>UINT32</b>

The zero-based starting character position of a substring in this instance.

### -param length

Type: [in] <b>UINT32</b>

The number of characters in the substring.

### -param newString

Type: [out] <b>[**HSTRING**](/windows/win32/winrt/hstring)*</b>

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

Each call to the <b>WindowsSubstringWithSpecifiedLength</b> function must be matched with a corresponding call to <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>


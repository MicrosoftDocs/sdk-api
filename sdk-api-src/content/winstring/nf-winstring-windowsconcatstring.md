---
UID: NF:winstring.WindowsConcatString
title: WindowsConcatString function (winstring.h)
description: Concatenates two specified strings.
helpviewer_keywords: ["WindowsConcatString","WindowsConcatString function [Windows Runtime]","winrt.windowsconcatstring","winstring/WindowsConcatString"]
old-location: winrt\windowsconcatstring.htm
tech.root: WinRT
ms.assetid: 916E1FC2-CCA1-4B4E-8710-99D5ECA31ABE
ms.date: 12/05/2018
ms.keywords: WindowsConcatString, WindowsConcatString function [Windows Runtime], winrt.windowsconcatstring, winstring/WindowsConcatString
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
 - WindowsConcatString
 - winstring/WindowsConcatString
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
 - WindowsConcatString
---

## -description

Concatenates two specified strings.

## -parameters

### -param string1

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The first string to be concatenated.

### -param string2

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The second string to be concatenated.

### -param newString

Type: [out] <b>[**HSTRING**](/windows/win32/winrt/hstring)*</b>

The concatenation of <i>string1</i> and <i>string2</i>. If <i>string1</i> and <i>string2</i> are <b>NULL</b>, <i>newString</i> is <b>NULL</b>. If either <i>string1</i> or <i>string2</i> is <b>NULL</b>, <i>newString</i> is a copy of the non-null string.

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
The  concatenated string was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>newString</i> is <b>NULL</b>, or the length of <i>string1</i> plus the length of <i>string2</i> is greater than <b>MAXUINT32</b>, which is  4,294,967,295; that is, hexadecimal 0xFFFFFFFF.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the concatenated string.

</td>
</tr>
</table>

## -remarks

Each call to the <b>WindowsConcatString</b> function must be matched with a corresponding call to <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>


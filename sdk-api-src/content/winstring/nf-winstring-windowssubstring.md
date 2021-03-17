---
UID: NF:winstring.WindowsSubstring
title: WindowsSubstring function (winstring.h)
description: Retrieves a substring from the specified string. The substring starts at the specified character position.
helpviewer_keywords: ["WindowsSubstring","WindowsSubstring function [Windows Runtime]","winrt.windowssubstring","winstring/WindowsSubstring"]
old-location: winrt\windowssubstring.htm
tech.root: WinRT
ms.assetid: 15DB3383-D7EC-4047-A1B8-90F8A47428EE
ms.date: 12/05/2018
ms.keywords: WindowsSubstring, WindowsSubstring function [Windows Runtime], winrt.windowssubstring, winstring/WindowsSubstring
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
 - WindowsSubstring
 - winstring/WindowsSubstring
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
 - WindowsSubstring
---

## -description

Retrieves a substring from the specified string. The substring starts at the specified character position.

## -parameters

### -param string

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The original string.

### -param startIndex

Type: [in] <b>UINT32</b>

The zero-based starting character position of a substring in this instance.

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
<i>newString</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
<i>startIndex</i> is greater than the length of <i>string</i>.

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

Each call to the <b>WindowsSubstring</b> function must be matched with a corresponding call to <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>


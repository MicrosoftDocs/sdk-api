---
UID: NF:winstring.WindowsDuplicateString
title: WindowsDuplicateString function (winstring.h)
description: Creates a copy of the specified string.
helpviewer_keywords: ["WindowsDuplicateString","WindowsDuplicateString function [Windows Runtime]","winrt.windowsduplicatestring","winstring/WindowsDuplicateString"]
old-location: winrt\windowsduplicatestring.htm
tech.root: WinRT
ms.assetid: 65343F8A-ACD5-4BD2-83CD-DA9F71690DF3
ms.date: 12/05/2018
ms.keywords: WindowsDuplicateString, WindowsDuplicateString function [Windows Runtime], winrt.windowsduplicatestring, winstring/WindowsDuplicateString
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
 - WindowsDuplicateString
 - winstring/WindowsDuplicateString
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
 - WindowsDuplicateString
---

## -description

Creates a copy of the specified string.

## -parameters

### -param string

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The string to be copied.

### -param newString

Type: [out] <b>[**HSTRING**](/windows/win32/winrt/hstring)*</b>

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
The <a href="/windows/win32/winrt/hstring"><b>HSTRING</b></a> was copied successfully.

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
Failed to allocate the new <a href="/windows/win32/winrt/hstring"><b>HSTRING</b></a>.

</td>
</tr>
</table>

## -remarks

Use the <b>WindowsDuplicateString</b>  function to copy an [**HSTRING**](/windows/win32/winrt/hstring). If <i>string</i> was created by calling the <a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestring">WindowsCreateString</a> function, the reference count of the backing buffer is incremented. If <i>string</i> was created by calling the <a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestringreference">WindowsCreateStringReference</a> function,  the Windows Runtime copies its source string to a new buffer and starts a reference count, which means that  <i>newString</i> is not a fast-pass string. 

Each call to the <b>WindowsDuplicateString</b> function must be matched with a corresponding call to <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestring">WindowsCreateString</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestringreference">WindowsCreateStringReference</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>


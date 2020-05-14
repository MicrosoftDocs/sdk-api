---
UID: NF:winstring.WindowsTrimStringEnd
title: WindowsTrimStringEnd function (winstring.h)
description: Removes all trailing occurrences of a specified set of characters from the source string.
helpviewer_keywords: ["WindowsTrimStringEnd","WindowsTrimStringEnd function [Windows Runtime]","winrt.windowstrimstringend","winstring/WindowsTrimStringEnd"]
old-location: winrt\windowstrimstringend.htm
tech.root: WinRT
ms.assetid: C6DC080D-04EA-43DF-AD6F-58419D4EB1B2
ms.date: 12/05/2018
ms.keywords: WindowsTrimStringEnd, WindowsTrimStringEnd function [Windows Runtime], winrt.windowstrimstringend, winstring/WindowsTrimStringEnd
f1_keywords:
- winstring/WindowsTrimStringEnd
dev_langs:
- c++
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
- WindowsTrimStringEnd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Removes all trailing occurrences of a specified set of characters from the source string.

## -parameters

### -param string

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The string to be trimmed.

### -param trimString

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The characters to remove from <i>string</i>.

### -param newString

Type: [out] <b>[**HSTRING**](/windows/win32/winrt/hstring)*</b>

The string that remains after all occurrences of characters in the <i>trimString</i> parameter are removed from the end of <i>string</i>, or <b>NULL</b> if <i>trimString</i> contains all of the characters in <i>string</i>.

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
The  trimmed string was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>newString</i> is <b>NULL</b>, or <i>trimString</i> is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the trimmed string.

</td>
</tr>
</table>

## -remarks

Each call to the <b>WindowsTrimStringEnd</b> function must be matched with a corresponding call to <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>
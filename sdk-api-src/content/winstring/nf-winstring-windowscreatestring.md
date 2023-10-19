---
UID: NF:winstring.WindowsCreateString
title: WindowsCreateString function (winstring.h)
description: Creates a new HSTRING based on the specified source string.
helpviewer_keywords: ["WindowsCreateString","WindowsCreateString function [Windows Runtime]","winrt.windowscreatestring","winstring/WindowsCreateString"]
old-location: winrt\windowscreatestring.htm
tech.root: WinRT
ms.assetid: CACEFB80-A47E-45A7-9E13-29C1326B9453
ms.date: 12/05/2018
ms.keywords: WindowsCreateString, WindowsCreateString function [Windows Runtime], winrt.windowscreatestring, winstring/WindowsCreateString
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
 - WindowsCreateString
 - winstring/WindowsCreateString
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
 - WindowsCreateString
---

## -description

Creates a new [**HSTRING**](/windows/win32/winrt/hstring) based on the specified source string.

## -parameters

### -param sourceString

Type: [in, optional] <b>LPCWSTR</b>

A null-terminated string to use as the source for the new [**HSTRING**](/windows/win32/winrt/hstring). To create a new, empty, or <b>NULL</b> string, pass <b>NULL</b> for <i>sourceString</i> and 0 for <i>length</i>.

### -param length

Type: [in] <b>UINT32</b>

The length of <i>sourceString</i>, in Unicode characters. Must be 0 if <i>sourceString</i> is <b>NULL</b>.

### -param string

Type: [out] <b>[**HSTRING**](/windows/win32/winrt/hstring)*</b>

A pointer to the newly created [**HSTRING**](/windows/win32/winrt/hstring), or <b>NULL</b> if an error occurs. Any existing  content in <i>string</i> is overwritten. The <b>HSTRING</b> is a standard handle type.

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
The <a href="/windows/win32/winrt/hstring"><b>HSTRING</b></a> was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>string</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the new <a href="/windows/win32/winrt/hstring"><b>HSTRING</b></a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>sourceString</i> is <b>NULL</b> and <i>length</i> is non-zero.

</td>
</tr>
</table>

## -remarks

Use the <b>WindowsCreateString</b> function to allocate a new [**HSTRING**](/windows/win32/winrt/hstring). The Windows Runtime copies <i>string</i> to the backing buffer of the new <b>HSTRING</b> and   manages the buffer lifetime by using a reference count. Call the <a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestringreference">WindowsCreateStringReference</a> function to create a <i>fast-pass string</i>, which uses an existing string without copying it. 

Call the <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a> function to de-allocate the [**HSTRING**](/windows/win32/winrt/hstring). Each call to the <b>WindowsCreateString</b> function must be matched by a call to  <b>WindowsDeleteString</b>. 

To create a new, empty, or <b>NULL</b> string, pass <b>NULL</b> for <i>sourceString</i> and 0 for <i>length</i>.

If <i>sourceString</i> has embedded null characters, the <b>WindowsCreateString</b> function copies all characters to the terminating null character.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestringreference">WindowsCreateStringReference</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>


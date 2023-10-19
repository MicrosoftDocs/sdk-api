---
UID: NF:winstring.WindowsCreateStringReference
title: WindowsCreateStringReference function (winstring.h)
description: Creates a new string reference based on the specified string.
helpviewer_keywords: ["WindowsCreateStringReference","WindowsCreateStringReference function [Windows Runtime]","winrt.windowscreatestringreference","winstring/WindowsCreateStringReference"]
old-location: winrt\windowscreatestringreference.htm
tech.root: WinRT
ms.assetid: 0361BB7E-DA49-4289-A93E-DE7AAB8712AC
ms.date: 12/05/2018
ms.keywords: WindowsCreateStringReference, WindowsCreateStringReference function [Windows Runtime], winrt.windowscreatestringreference, winstring/WindowsCreateStringReference
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
 - WindowsCreateStringReference
 - winstring/WindowsCreateStringReference
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
 - WindowsCreateStringReference
---

## -description

Creates a new string reference based on the specified string.

## -parameters

### -param sourceString

Type: [in] <b>PCWSTR</b>

A null-terminated string to use as the source for the new [**HSTRING**](/windows/win32/winrt/hstring).

A value of <b>NULL</b> represents the empty string, if the value of <i>length</i> is 0. Should be allocated on the stack frame.

### -param length

Type: [in] <b>UINT32</b>

The length of <i>sourceString</i>, in Unicode characters. Must be 0 if <i>sourceString</i> is <b>NULL</b>. If greater than 0, <i>sourceString</i> must have a terminating null character.

### -param hstringHeader

Type: [out] <b><a href="/windows/desktop/api/hstring/ns-hstring-hstring_header">HSTRING_HEADER</a>*</b>

A pointer to a structure that the Windows Runtime uses to identify <i>string</i> as a string reference, or fast-pass string.

### -param string

Type: [out] <b>[**HSTRING**](/windows/win32/winrt/hstring)*</b>

A pointer to the newly created string, or <b>NULL</b> if an error occurs. Any existing  content in <i>string</i> is overwritten. The [**HSTRING**](/windows/win32/winrt/hstring) is a standard handle type.

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
Either <i>string</i> or <i>hstringHeader</i>  is <b>NULL</b>, or <i>string</i> is not null-terminated.

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

Use the <b>WindowsCreateStringReference</b> function to create an [**HSTRING**](/windows/win32/winrt/hstring) from an existing string. This kind of <b>HSTRING</b> is named a <i>fast-pass string</i>. Unlike an <b>HSTRING</b> created by the <a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestring">WindowsCreateString</a> function, the lifetime of the backing buffer in the new <b>HSTRING</b> is  not managed by the Windows Runtime.  The caller allocates <i>sourceString</i> on the  stack frame, together with an uninitialized <a href="/windows/desktop/api/hstring/ns-hstring-hstring_header">HSTRING_HEADER</a>, to avoid a heap allocation and eliminate the risk of a memory leak. The caller must ensure that <i>sourceString</i> and the contents of <i>hstringHeader</i> remain unchanged during the lifetime of the attached <b>HSTRING</b>.

You don't need to call the <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a> function to de-allocate a fast-pass [**HSTRING**](/windows/win32/winrt/hstring) created by the <b>WindowsCreateStringReference</b> function.

To create an empty [**HSTRING**](/windows/win32/winrt/hstring), pass <b>NULL</b> for <i>sourceString</i> and 0 for <i>length</i>. 

The Windows Runtime tracks a fast-pass string by using an <a href="/windows/desktop/api/hstring/ns-hstring-hstring_header">HSTRING_HEADER</a> structure, which is returned in the <i>hstringHeader</i> out parameter. Do not change the contents of the <b>HSTRING_HEADER</b>.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestring">WindowsCreateString</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>


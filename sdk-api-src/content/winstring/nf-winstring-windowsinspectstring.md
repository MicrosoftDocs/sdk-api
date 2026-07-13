---
UID: NF:winstring.WindowsInspectString
title: WindowsInspectString function (winstring.h)
description: Provides a way to for debuggers to display the value of a Windows Runtime HSTRING in another address space, remotely, or from a dump. (WindowsInspectString)
helpviewer_keywords: ["WindowsInspectString","WindowsInspectString function [Windows Runtime]","winrt.windowsinspectstring","winstring/WindowsInspectString"]
old-location: winrt\windowsinspectstring.htm
tech.root: WinRT
ms.assetid: DB1A35D3-D7DF-439F-B4C2-9510FC1977E9
ms.date: 12/05/2018
ms.keywords: WindowsInspectString, WindowsInspectString function [Windows Runtime], winrt.windowsinspectstring, winstring/WindowsInspectString
req.header: winstring.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WindowsInspectString
 - winstring/WindowsInspectString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-String-l1-1-0.dll
 - API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
 - WindowsInspectString
---

## -description

Provides a way to for debuggers to display the value of a Windows Runtime [**HSTRING**](/windows/win32/winrt/hstring) in another address space, remotely, or from a dump.

## -parameters

### -param targetHString

[in]

The [**HSTRING**](/windows/win32/winrt/hstring) to inspect.

### -param machine

The format of the target address space. Valid values are <b>IMAGE_FILE_MACHINE_AMD64</b> for Win64,  <b>IMAGE_FILE_MACHINE_I386</b> for  Win32, or <b>IMAGE_FILE_MACHINE_ARM</b> for 32-bit ARM.

### -param callback

[in]

A callback function to read the string buffer from the target address space. This function is called before the <i>length</i> and <i>targetStringAddress</i> parameters are computed by the <b>WindowsInspectString</b> function.

### -param context

[in, optional]

Custom context data passed to the callback.

### -param length

[out]

The length of the string in the target address space, if the call to <i>callback</i> is successful; otherwise, 0.

### -param targetStringAddress

[out]

The target address of the raw <b>PCWSTR</b>, if the call to <i>callback</i> is successful; otherwise, <b>NULL</b>.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

<ul>
<li><b>IMAGE_FILE_MACHINE_AMD64</b> was specified for <i>machine</i>, but the current platform is not Win64, or</li>
<li><i>machine</i> is not <b>IMAGE_FILE_MACHINE_AMD64</b>,  <b>IMAGE_FILE_MACHINE_I386</b>, or <b>IMAGE_FILE_MACHINE_ARM</b>, or</li>
<li><i>targetHString</i> is not a correctly formed <a href="/windows/win32/winrt/hstring"><b>HSTRING</b></a>. </li>
</ul>

</td>
</tr>
</table>

## -see-also

[**HSTRING**](/windows/win32/winrt/hstring)

<a href="/windows/desktop/api/winstring/nc-winstring-pinspect_hstring_callback">PINSPECT_HSTRING_CALLBACK</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestring">WindowsCreateString</a>


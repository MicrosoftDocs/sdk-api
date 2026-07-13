---
UID: NF:winstring.WindowsInspectString2
title: WindowsInspectString2 function (winstring.h)
description: Provides a way to for debuggers to display the value of a Windows Runtime HSTRING in another address space, remotely, or from a dump. (WindowsInspectString2)
helpviewer_keywords: ["WindowsInspectString2","WindowsInspectString2 function [Windows Runtime]","winrt.windowsinspectstring2","winstring/WindowsInspectString2"]
old-location: winrt\windowsinspectstring2.htm
tech.root: WinRT
ms.assetid: 6A359C2A-21A3-4DCD-B40A-B983E790AC3C
ms.date: 12/05/2018
ms.keywords: WindowsInspectString2, WindowsInspectString2 function [Windows Runtime], winrt.windowsinspectstring2, winstring/WindowsInspectString2
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
 - WindowsInspectString2
 - winstring/WindowsInspectString2
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
 - WindowsInspectString2
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

A callback function to read the string buffer from the target address space. This function is called before the <i>length</i> and <i>targetStringAddress</i> parameters are computed by the <b>WindowsInspectString2</b> function.

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
<li>The <i>machine</i> value is not <b>IMAGE_FILE_MACHINE_AMD64</b>,  <b>IMAGE_FILE_MACHINE_I386</b>, or <b>IMAGE_FILE_MACHINE_ARM</b> or</li>
<li><i>targetHString</i> is not a correctly formed <a href="/windows/win32/winrt/hstring"><b>HSTRING</b></a>. </li>
</ul>

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/winstring/nf-winstring-windowsinspectstring">WindowsInspectString</a> function passes the input and output pointers as native pointer-sized values. If  the current platform is Win32, that function returns an error for processes that are Win64. 

<b>WindowsInspectString2</b> enables cross-architecture debugging by allowing up to 64-bit values when called from both Win32 and Win64 applications.

## -see-also

[**HSTRING**](/windows/win32/winrt/hstring)

<a href="/windows/desktop/api/winstring/nc-winstring-pinspect_hstring_callback">PINSPECT_HSTRING_CALLBACK</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestring">WindowsCreateString</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowsinspectstring">WindowsInspectString</a>


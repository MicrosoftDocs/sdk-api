---
UID: NF:winstring.WindowsDeleteString
title: WindowsDeleteString function (winstring.h)
description: Decrements the reference count of a string buffer.
helpviewer_keywords: ["WindowsDeleteString","WindowsDeleteString function [Windows Runtime]","winrt.windowsdeletestring","winstring/WindowsDeleteString"]
old-location: winrt\windowsdeletestring.htm
tech.root: WinRT
ms.assetid: 79B9E5CF-396C-45FB-931B-7B50281A0446
ms.date: 12/05/2018
ms.keywords: WindowsDeleteString, WindowsDeleteString function [Windows Runtime], winrt.windowsdeletestring, winstring/WindowsDeleteString
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
 - WindowsDeleteString
 - winstring/WindowsDeleteString
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
 - WindowsDeleteString
---

## -description

Decrements the reference count of a string buffer.

## -parameters

### -param string

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The string to be deleted. If <i>string</i> is a fast-pass string created by <a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestringreference">WindowsCreateStringReference</a>, or if <i>string</i> is <b>NULL</b> or empty, no action is taken and <b>S_OK</b> is returned.

## -returns

Type: <b>HRESULT</b>

This function always returns <b>S_OK</b>.

## -remarks

Use the <b>WindowsDeleteString</b> function to de-allocate an [**HSTRING**](/windows/win32/winrt/hstring). Calling <b>WindowsDeleteString</b> decrements the reference count of the backing buffer, and if the reference count reaches 0, the Windows Runtime de-allocates the buffer.

## -see-also

<a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestring">WindowsCreateString</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowscreatestringreference">WindowsCreateStringReference</a>


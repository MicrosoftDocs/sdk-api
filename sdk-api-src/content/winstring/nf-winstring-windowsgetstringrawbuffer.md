---
UID: NF:winstring.WindowsGetStringRawBuffer
title: WindowsGetStringRawBuffer function (winstring.h)
description: Retrieves the backing buffer for the specified string.
helpviewer_keywords: ["WindowsGetStringRawBuffer","WindowsGetStringRawBuffer function [Windows Runtime]","winrt.windowsgetstringrawbuffer","winstring/WindowsGetStringRawBuffer"]
old-location: winrt\windowsgetstringrawbuffer.htm
tech.root: WinRT
ms.assetid: D2906CD0-7529-459E-A0E9-66D29A5DD1B0
ms.date: 01/27/2022
ms.keywords: WindowsGetStringRawBuffer, WindowsGetStringRawBuffer function [Windows Runtime], winrt.windowsgetstringrawbuffer, winstring/WindowsGetStringRawBuffer
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
 - WindowsGetStringRawBuffer
 - winstring/WindowsGetStringRawBuffer
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
 - WindowsGetStringRawBuffer
---

## -description

Retrieves the backing buffer for the specified string.

## -parameters

### -param string

Type: [in, optional] **[HSTRING](/windows/win32/winrt/hstring)**

An optional string for which the backing buffer is to be retrieved. Can be **NULL**.

### -param length

Type: [out, optional] **UINT32 \***

An optional pointer to a **UINT32**. If **NULL** is passed for *length*, then it is ignored. If *length* is a valid pointer to a **UINT32**, and *string* is a valid [**HSTRING**](/windows/win32/winrt/hstring), then on successful completion the function sets the value pointed to by *length* to the number of Unicode characters in the backing buffer for *string* (including embedded null characters, but excluding the terminating null). If *length* is a valid pointer to a **UINT32**, and *string* is **NULL**, then the value pointed to by *length* is set to 0.

## -returns

Type: <b>PCWSTR</b>

A pointer to the buffer that provides the backing store for <i>string</i>, or the empty string if <i>string</i> is <b>NULL</b> or the empty string.

## -remarks

Use the <b>WindowsGetStringRawBuffer</b> function to obtain a pointer to the backing buffer of an [**HSTRING**](/windows/win32/winrt/hstring).

Don't change the contents of the buffer&mdash;an [**HSTRING**](/windows/win32/winrt/hstring) is required to be immutable.


---
UID: NF:winstring.WindowsGetStringLen
title: WindowsGetStringLen function (winstring.h)
description: Gets the length, in Unicode characters, of the specified string.
helpviewer_keywords: ["WindowsGetStringLen","WindowsGetStringLen function [Windows Runtime]","winrt.windowsgetstringlen","winstring/WindowsGetStringLen"]
old-location: winrt\windowsgetstringlen.htm
tech.root: WinRT
ms.assetid: 80B659DF-C760-4D9E-B779-144A5B8FEA59
ms.date: 12/05/2018
ms.keywords: WindowsGetStringLen, WindowsGetStringLen function [Windows Runtime], winrt.windowsgetstringlen, winstring/WindowsGetStringLen
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
 - WindowsGetStringLen
 - winstring/WindowsGetStringLen
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
 - WindowsGetStringLen
---

## -description

Gets the length, in Unicode characters, of the specified string.

## -parameters

### -param string

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The string whose length is to be found.

## -returns

Type: <b>UINT32</b>

The number of Unicode characters in <i>string</i>, including embedded null characters, but excluding the terminating null; or 0 if <i>string</i> is <b>NULL</b>.


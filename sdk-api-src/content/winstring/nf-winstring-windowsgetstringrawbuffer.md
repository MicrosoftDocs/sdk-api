---
UID: NF:winstring.WindowsGetStringRawBuffer
title: WindowsGetStringRawBuffer function (winstring.h)
description: Gets the backing buffer for the specified string.helpviewer_keywords: ["WindowsGetStringRawBuffer","WindowsGetStringRawBuffer function [Windows Runtime]","winrt.windowsgetstringrawbuffer","winstring/WindowsGetStringRawBuffer"]
old-location: winrt\windowsgetstringrawbuffer.htm
tech.root: WinRT
ms.assetid: D2906CD0-7529-459E-A0E9-66D29A5DD1B0
ms.date: 12/05/2018
ms.keywords: WindowsGetStringRawBuffer, WindowsGetStringRawBuffer function [Windows Runtime], winrt.windowsgetstringrawbuffer, winstring/WindowsGetStringRawBuffer
f1_keywords:
- winstring/WindowsGetStringRawBuffer
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
- WindowsGetStringRawBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WindowsGetStringRawBuffer function


## -description


Gets the backing buffer for the specified string.


## -parameters




### -param string [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a></b>

The string for which the backing buffer is to be retrieved.


### -param length [out, optional]

Type: <b>UINT32*</b>

The number of Unicode characters in the backing buffer for <i>string</i>, including embedded null characters, but excluding the terminating null; or 0 if <i>string</i> is <b>NULL</b>.


## -returns



Type: <b>PCWSTR</b>

A pointer to the buffer that provides the backing store for <i>string</i>, or the empty string if  <i>string</i> is <b>NULL</b> or the empty string.




## -remarks



Use the <b>WindowsGetStringRawBuffer</b>  function to obtain a pointer to the backing buffer of  an <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>.

Do not change the contents of the buffer as all  <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRINGs</a> are required to be immutable.




---
UID: NF:winstring.WindowsGetStringRawBuffer
title: WindowsGetStringRawBuffer function
author: windows-sdk-content
description: Gets the backing buffer for the specified string.
old-location: winrt\windowsgetstringrawbuffer.htm
tech.root: WinRT
ms.assetid: D2906CD0-7529-459E-A0E9-66D29A5DD1B0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WindowsGetStringRawBuffer, WindowsGetStringRawBuffer function [Windows Runtime], winrt.windowsgetstringrawbuffer, winstring/WindowsGetStringRawBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WindowsGetStringRawBuffer function


## -description


Gets the backing buffer for the specified string.


## -parameters




### -param string [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The string for which the backing buffer is to be retrieved.


### -param length [out, optional]

Type: <b>UINT32*</b>

The number of Unicode characters in the backing buffer for <i>string</i>, including embedded null characters, but excluding the terminating null; or 0 if <i>string</i> is <b>NULL</b>.


## -returns



Type: <b>PCWSTR</b>

A pointer to the buffer that provides the backing store for <i>string</i>, or the empty string if  <i>string</i> is <b>NULL</b> or the empty string.




## -remarks



Use the <b>WindowsGetStringRawBuffer</b>  function to obtain a pointer to the backing buffer of  an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>.

Do not change the contents of the buffer as all  <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRINGs</a> are required to be immutable.




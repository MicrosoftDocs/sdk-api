---
UID: NF:winternl.RtlCharToInteger
title: RtlCharToInteger function
author: windows-sdk-content
description: Converts a character string to an integer.
old-location: winprog\rtlchartointeger.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlchartointeger.htm
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: RtlCharToInteger, RtlCharToInteger function [Windows API], winprog.rtlchartointeger, winternl/RtlCharToInteger, winui.rtlchartointeger
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SYNC_VERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ntdll.dll
api_name:
 - RtlCharToInteger
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlCharToInteger function


## -description


Converts a character string to an integer.


## -parameters




### -param String [in]

A pointer to the string to convert. The format of the string is as follows: 

[whitespace] [{+ | -}] [0 [{x | o | b}]] [digits]


### -param Base [in, optional]

<b>ULONG</b> that contains the number base to use for the conversion, such as base 10. Only base 2, 8, 10, and 16 are supported.


### -param Value [out]

A pointer to a <b>ULONG</b> that receives the integer that resulted from the conversion.


## -returns



If the function succeeds, the function returns <b>STATUS_SUCCESS</b>.




## -remarks



When converting strings to integers the preferred function to use is <a href="https://msdn.microsoft.com/library/windows/desktop/1787c96a-f283-4a83-9325-33cfc1c7e240">strtol, wcstol</a>.

There is no import library for this function. Use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> rather than linking to the function directly.




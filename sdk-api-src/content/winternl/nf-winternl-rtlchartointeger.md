---
UID: NF:winternl.RtlCharToInteger
title: RtlCharToInteger function (winternl.h)
description: Converts a character string to an integer.
helpviewer_keywords: ["RtlCharToInteger","RtlCharToInteger function [Windows API]","winprog.rtlchartointeger","winternl/RtlCharToInteger","winui.rtlchartointeger"]
old-location: winprog\rtlchartointeger.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlchartointeger.htm
ms.date: 12/05/2018
ms.keywords: RtlCharToInteger, RtlCharToInteger function [Windows API], winprog.rtlchartointeger, winternl/RtlCharToInteger, winui.rtlchartointeger
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlCharToInteger
 - winternl/RtlCharToInteger
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ntdll.dll
api_name:
 - RtlCharToInteger
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

When converting strings to integers the preferred function to use is <a href="/previous-versions/visualstudio/visual-studio-2010/w4z2wdyc(v=vs.100)">strtol, wcstol</a>.

There is no import library for this function. Use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> rather than linking to the function directly.
---
UID: NF:winternl.RtlFreeUnicodeString
title: RtlFreeUnicodeString function
author: windows-sdk-content
description: Frees the string buffer allocated by RtlAnsiStringToUnicodeString or by RtlUpcaseUnicodeString.
old-location: winprog\rtlfreeunicodestring.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlfreeunicodestring.htm
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: RtlFreeUnicodeString, RtlFreeUnicodeString function [Windows API], winprog.rtlfreeunicodestring, winternl/RtlFreeUnicodeString, winui.rtlfreeunicodestring
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: NtosKrnl.lib
req.dll: Ntdll.dll; NtosKrnl.exe
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
 - NtosKrnl.exe
api_name:
 - RtlFreeUnicodeString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlFreeUnicodeString function


## -description


Frees the string buffer allocated by
    <a href="https://msdn.microsoft.com/en-us/library/ms648413(v=VS.85).aspx">RtlAnsiStringToUnicodeString</a> or by <b>RtlUpcaseUnicodeString</b>.


## -parameters




### -param UnicodeString [in, out]

A pointer to the Unicode string whose
        buffer was previously allocated by <a href="https://msdn.microsoft.com/en-us/library/ms648413(v=VS.85).aspx">RtlAnsiStringToUnicodeString</a>.


## -returns



This function does not return a value.




## -remarks



This routine does not release the ANSI string buffer passed to <a href="https://msdn.microsoft.com/en-us/library/ms648413(v=VS.85).aspx">RtlAnsiStringToUnicodeString</a> or <b>RtlUpcaseUnicodeString</b>.
		

Because there is no import library for this function, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.
		




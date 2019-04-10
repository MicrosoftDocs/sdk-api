---
UID: NF:psapi.EnumProcesses
title: EnumProcesses function (psapi.h)
author: windows-sdk-content
description: Retrieves the process identifier for each process object in the system.
old-location: psapi\enumprocesses.htm
tech.root: psapi
ms.assetid: 0c0445cb-27d2-4857-a4a5-7a4c180b068b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumProcesses, EnumProcesses function [PSAPI], K32EnumProcesses, _win32_enumprocesses, base.enumprocesses, psapi.enumprocesses, psapi/EnumProcesses, psapi/K32EnumProcesses
ms.topic: function
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Psapi.dll
 - Psapi.dll
 - API-MS-Win-Core-PsAPI-L1-1-0.dll
 - KernelBase.dll
api_name:
 - EnumProcesses
 - K32EnumProcesses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumProcesses function


## -description


Retrieves the process identifier for each process object in the system.


## -parameters




### -param lpidProcess [out]

A pointer to an array that receives the list of process identifiers.


### -param cb [in]

The size of the <i>pProcessIds</i> array, in bytes.


### -param lpcbNeeded [out]

The number of bytes returned in the <i>pProcessIds</i> array.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



It is a good idea to use a large array, because it is hard to predict how many processes there will be at the time you call 
<b>EnumProcesses</b>. 

To determine how many processes were enumerated, divide the <i>pBytesReturned</i> value by sizeof(DWORD). There is no indication given when the buffer is too small to store all process identifiers. Therefore, if <i>pBytesReturned</i> equals <i>cb</i>, consider retrying the call with a larger array.

To obtain process handles for the processes whose identifiers you have just obtained, call the <a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a> function.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes version numbers for the PSAPI functions. The PSAPI version number affects  the name used to call the function and the library that a program must load. 

If PSAPI_VERSION is 2 or greater, this function is defined as <b>K32EnumProcesses</b> in Psapi.h and exported in Kernel32.lib and Kernel32.dll. If PSAPI_VERSION is 1, this function is defined as <b>EnumProcesses</b> in Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls <b>K32EnumProcesses</b>. 

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions should always call this function as <b>EnumProcesses</b>. To ensure correct resolution of symbols, add Psapi.lib to the TARGETLIBS macro and compile the program with –DPSAPI_VERSION=1. To use run-time dynamic linking, load Psapi.dll.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/0ed81548-4936-40e9-bfc8-baa71492310e">Enumerating All Processes</a> or 
<a href="https://msdn.microsoft.com/2e411eba-ba60-4678-bf6f-bc15b6e8b478">Enumerating All Modules for a Process</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>



<a href="https://msdn.microsoft.com/229c661e-9c33-47a3-9441-558cfe2a800d">Process Information</a>
 

 


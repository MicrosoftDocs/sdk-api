---
UID: NF:psapi.EmptyWorkingSet
title: EmptyWorkingSet function
author: windows-sdk-content
description: Removes as many pages as possible from the working set of the specified process.
old-location: psapi\emptyworkingset.htm
tech.root: psapi
ms.assetid: 76f2252e-7305-46b0-b1af-40ac084e6696
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EmptyWorkingSet, EmptyWorkingSet function [PSAPI], K32EmptyWorkingSet, _win32_emptyworkingset, base.emptyworkingset, psapi.emptyworkingset, psapi/EmptyWorkingSet, psapi/K32EmptyWorkingSet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - EmptyWorkingSet
 - K32EmptyWorkingSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EmptyWorkingSet function


## -description


Removes as many pages as possible from the working set of the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right and the <b>PROCESS_SET_QUOTA</b> access right. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You can also empty the working set by calling  the <a href="https://msdn.microsoft.com/8bc0053c-f687-43b5-a435-df1e813a5204">SetProcessWorkingSetSize</a> or <a href="https://msdn.microsoft.com/04332239-dfc2-4d32-987a-af187e725b71">SetProcessWorkingSetSizeEx</a> function with the <i>dwMinimumWorkingSetSize</i> and <i>dwMaximumWorkingSetSize</i> parameters set to the value <code>(SIZE_T)(-1)</code>.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32EmptyWorkingSet</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as K32EmptyWorkingSet in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32EmptyWorkingSet</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    K32EmptyWorkingSet. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.




## -see-also




<a href="https://msdn.microsoft.com/0c0445cb-27d2-4857-a4a5-7a4c180b068b">EnumProcesses</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>



<a href="https://msdn.microsoft.com/8bc0053c-f687-43b5-a435-df1e813a5204">SetProcessWorkingSetSize</a>



<a href="https://msdn.microsoft.com/ff05276a-1d40-4844-b649-10e32e3f1937">Working Set</a>



<a href="https://msdn.microsoft.com/33c42f79-cc77-4d44-84c3-8bf0a4a60019">Working Set Information</a>
 

 


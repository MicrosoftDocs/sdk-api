---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# QueryWorkingSetEx function


## -description


Retrieves extended information about the pages at specific virtual addresses in the address space of 
    the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and 
      <b>PROCESS_VM_READ</b> access rights. For more information, see 
      <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param pv [in, out]

A pointer to an array of 
      <a href="https://msdn.microsoft.com/d3500737-b9af-41a8-bf69-61d0bfbd6ce4">PSAPI_WORKING_SET_EX_INFORMATION</a> 
      structures. On input, each item in the array specifies a virtual address of interest. On output, each item in 
      the array receives information about the corresponding virtual page.


### -param cb [in]

The size of the <i>pv</i> buffer, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Unlike the <a href="https://msdn.microsoft.com/b932153f-2bbd-460e-8ff7-b3e493c397bb">QueryWorkingSet</a> function, which is 
    limited to the working set of the target process, the 
    <b>QueryWorkingSetEx</b> function can be used to query 
    addresses that are not in the process working set but are still part of the process, such as AWE and large 
    pages.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32QueryWorkingSetEx</b> in Psapi.h and exported in Kernel32.lib 
    and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this function is defined as 
    <b>QueryWorkingSetEx</b> in Psapi.h and 
    exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32QueryWorkingSetEx</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions should always 
    call this function as <b>QueryWorkingSetEx</b>. To ensure 
    correct resolution of symbols, add Psapi.lib to the <b>TARGETLIBS</b> macro 
    and compile the program with "–DPSAPI_VERSION=1". To use run-time dynamic 
    linking, load Psapi.dll.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/df025b35-fb6b-4987-806e-9c76e6b130a1">Allocating Memory from a NUMA Node</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c0445cb-27d2-4857-a4a5-7a4c180b068b">EnumProcesses</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>



<a href="https://msdn.microsoft.com/d3500737-b9af-41a8-bf69-61d0bfbd6ce4">PSAPI_WORKING_SET_EX_INFORMATION</a>



<a href="https://msdn.microsoft.com/33c42f79-cc77-4d44-84c3-8bf0a4a60019">Working Set Information</a>
 

 


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

# QueryWorkingSet function


## -description


Retrieves information about the pages currently added to the working set of the specified 
    process.

To retrieve working set information for a subset of virtual addresses, or to retrieve information about pages 
    that are not part of the working set (such as AWE or large pages), use the 
    <a href="https://msdn.microsoft.com/59ae76c9-e954-4648-9c9f-787136375b02">QueryWorkingSetEx</a> function.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and 
      <b>PROCESS_VM_READ</b> access rights. For more information, see 
      <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param pv [out]

A pointer to the buffer that receives the information. For more information, see 
       <a href="https://msdn.microsoft.com/59ca42c0-ca88-4153-b061-980d961a8ca2">PSAPI_WORKING_SET_INFORMATION</a>.

If the buffer pointed to by the <i>pv</i> parameter is not large enough to contain all 
       working set entries for the target process, the function fails with <b>ERROR_BAD_LENGTH</b>. 
       In this case, the <b>NumberOfEntries</b> member of the 
       <a href="https://msdn.microsoft.com/59ca42c0-ca88-4153-b061-980d961a8ca2">PSAPI_WORKING_SET_INFORMATION</a> 
       structure is set to the required number of entries, but the function does not return information about the 
       working set entries.


### -param cb [in]

The size of the <i>pv</i> buffer, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32QueryWorkingSet</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>QueryWorkingSet</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32QueryWorkingSet</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions 
    should always call this function as <b>QueryWorkingSet</b>. 
    To ensure correct resolution of symbols, add Psapi.lib to the 
    <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load 
    Psapi.dll.




## -see-also




<a href="https://msdn.microsoft.com/0c0445cb-27d2-4857-a4a5-7a4c180b068b">EnumProcesses</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>



<a href="https://msdn.microsoft.com/59ca42c0-ca88-4153-b061-980d961a8ca2">PSAPI_WORKING_SET_INFORMATION</a>



<a href="https://msdn.microsoft.com/59ae76c9-e954-4648-9c9f-787136375b02">QueryWorkingSetEx</a>



<a href="https://msdn.microsoft.com/33c42f79-cc77-4d44-84c3-8bf0a4a60019">Working Set Information</a>
 

 


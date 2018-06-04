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

# EnumPageFilesA function


## -description


Calls the callback routine for each installed pagefile in the system.


## -parameters




### -param pCallBackRoutine

TBD


### -param pContext

TBD




#### - lpContext [in]

The user-defined data passed to the callback routine.


#### - pCallbackRoutine [out]

A pointer to the routine called for each pagefile. For more information, see 
      <a href="https://msdn.microsoft.com/eb3610fb-2c95-4f7b-973d-8dc41d2829f1">EnumPageFilesProc</a>.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the 
       return value is <b>FALSE</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects  the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32EnumPageFiles</b> in Psapi.h and exported in Kernel32.lib and 
    Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this function is defined as 
    <b>EnumPageFiles</b> in Psapi.h and exported in 
    Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32EnumPageFiles</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions 
    should always call this function as <b>EnumPageFiles</b>. To 
    ensure correct resolution of symbols, add Psapi.lib to the <b>TARGETLIBS</b> 
    macro and compile the program with –DPSAPI_VERSION=1. To use run-time dynamic linking, load 
    Psapi.dll.




## -see-also




<a href="https://msdn.microsoft.com/eb3610fb-2c95-4f7b-973d-8dc41d2829f1">EnumPageFilesProc</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>
 

 


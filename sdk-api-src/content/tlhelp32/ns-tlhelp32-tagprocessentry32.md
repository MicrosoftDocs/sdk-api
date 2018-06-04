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

# tagPROCESSENTRY32 structure


## -description


Describes an entry from a list of the processes residing in the system address space when a snapshot was taken.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="https://msdn.microsoft.com/097790e8-30c2-4b00-9256-fa26e2ceb893">Process32First</a> function, set this member to <code>sizeof(PROCESSENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
<b>Process32First</b> fails.


### -field cntUsage

This member is no longer used and is always set to zero.


### -field th32ProcessID

The process identifier.


### -field th32DefaultHeapID

This member is no longer used and is always set to zero.


### -field th32ModuleID

This member is no longer used and is always set to zero.


### -field cntThreads

The number of execution threads started by the process.


### -field th32ParentProcessID

The identifier of the process that created this process (its parent process).


### -field pcPriClassBase

The base priority of any threads created by this process.


### -field dwFlags

This member is no longer used, and is always set to zero.


### -field szExeFile

The name of the executable file for the process. To retrieve the full path to the executable file, call the <a href="https://msdn.microsoft.com/bb41cab9-13a1-469d-bf76-68c172e982f6">Module32First</a> function and check the <b>szExePath</b> member of the <a href="https://msdn.microsoft.com/305fab35-625c-42e3-a434-e2513e4c8870">MODULEENTRY32</a> structure that is returned. However, if the calling process is a 32-bit process, you must call the <a href="https://msdn.microsoft.com/49a9d1aa-30f3-45ea-a4ec-9f55df692b8b">QueryFullProcessImageName</a> function to retrieve the full path of the executable file for a 64-bit process.


## -see-also




<a href="https://msdn.microsoft.com/097790e8-30c2-4b00-9256-fa26e2ceb893">Process32First</a>



<a href="https://msdn.microsoft.com/843a95fd-27ae-4215-83d0-82fc402b82b6">Process32Next</a>
 

 


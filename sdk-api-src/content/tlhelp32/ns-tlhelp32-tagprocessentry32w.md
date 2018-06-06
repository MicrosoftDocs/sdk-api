---
UID: NS:tlhelp32.tagPROCESSENTRY32W
title: tagPROCESSENTRY32W
author: windows-sdk-content
description: Describes an entry from a list of the processes residing in the system address space when a snapshot was taken.
old-location: toolhelp\processentry32_str.htm
old-project: ToolHelp
ms.assetid: 9e2f7345-52bf-4bfc-9761-90b0b374c727
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*LPPROCESSENTRY32W, *PPROCESSENTRY32W, PPROCESSENTRY32, PPROCESSENTRY32 structure pointer [ToolHelp], PROCESSENTRY32, PROCESSENTRY32 structure [ToolHelp], PROCESSENTRY32W, _win32_processentry32_str, base.processentry32_str, tagPROCESSENTRY32W, tlhelp32/PPROCESSENTRY32, tlhelp32/PROCESSENTRY32, tlhelp32/PROCESSENTRY32W, toolhelp.processentry32_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tlhelp32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PROCESSENTRY32W (Unicode) and PROCESSENTRY32 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PROCESSENTRY32W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TlHelp32.h
api_name:
 - PROCESSENTRY32
 - PROCESSENTRY32
 - PROCESSENTRY32W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# tagPROCESSENTRY32W structure


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
 

 


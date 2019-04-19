---
UID: NF:tlhelp32.Toolhelp32ReadProcessMemory
title: Toolhelp32ReadProcessMemory function (tlhelp32.h)
author: windows-sdk-content
description: Copies memory allocated to another process into an application-supplied buffer.
old-location: toolhelp\toolhelp32readprocessmemory.htm
tech.root: ToolHelp
ms.assetid: e579b813-32ef-481d-8dc6-f959ec9b6bad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Toolhelp32ReadProcessMemory, Toolhelp32ReadProcessMemory function [ToolHelp], _win32_toolhelp32readprocessmemory, base.toolhelp32readprocessmemory, tlhelp32/Toolhelp32ReadProcessMemory, toolhelp.toolhelp32readprocessmemory
ms.topic: function
req.header: tlhelp32.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - Toolhelp32ReadProcessMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Toolhelp32ReadProcessMemory function


## -description


Copies memory allocated to another process into an application-supplied buffer.


## -parameters




### -param th32ProcessID [in]

The identifier of the process whose memory is being copied. This parameter can be zero to copy the memory of the current process.


### -param lpBaseAddress [in]

The base address in the specified process to read. Before transferring any data, the system verifies that all data in the base address and memory of the specified size is accessible for read access. If this is the case, the function proceeds. Otherwise, the function fails.


### -param lpBuffer [out]

A pointer to a buffer that receives the contents of the address space of the specified process.


### -param cbRead [in]

The number of bytes to read from the specified process.


### -param lpNumberOfBytesRead [out]

The number of bytes copied to the specified buffer. If this parameter is <b>NULL</b>, it is ignored.


## -returns



Returns <b>TRUE</b> if successful.




## -see-also




<a href="https://msdn.microsoft.com/097790e8-30c2-4b00-9256-fa26e2ceb893">Process32First</a>



<a href="https://msdn.microsoft.com/843a95fd-27ae-4215-83d0-82fc402b82b6">Process32Next</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 


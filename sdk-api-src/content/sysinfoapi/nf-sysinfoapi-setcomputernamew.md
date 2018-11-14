---
UID: NF:sysinfoapi.SetComputerNameW
title: SetComputerNameW function
author: windows-sdk-content
description: Sets a new NetBIOS name for the local computer. The name is stored in the registry and the name change takes effect the next time the user restarts the computer.
old-location: base\setcomputername.htm
tech.root: sysinfo
ms.assetid: ff64fde2-d1b5-4211-b8c4-4823a5469e04
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: SetComputerName, SetComputerName function, SetComputerNameA, SetComputerNameW, _win32_setcomputername, base.setcomputername, sysinfoapi/SetComputerName, sysinfoapi/SetComputerNameA, sysinfoapi/SetComputerNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetComputerNameW (Unicode) and SetComputerNameA (ANSI)
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
 - API-Ms-Win-Core-SysInfo-L1-2-3.dll
 - KernelBase.dll
api_name:
 - SetComputerName
 - SetComputerNameA
 - SetComputerNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetComputerNameW
: 
---

# SetComputerNameW function


## -description


Sets a new NetBIOS name for the local computer. The name is stored in the registry and the name change takes effect the next time the user restarts the computer.

If the local computer is a node in a cluster, 
<b>SetComputerName</b> sets NetBIOS name of the local computer, not that of the cluster virtual server.

To set the DNS host name or the DNS domain name, call the 
<a href="https://msdn.microsoft.com/12163456-770c-4f9e-9261-a6ea5f2cd93a">SetComputerNameEx</a> function.


## -parameters




### -param lpComputerName [in]

The computer name that will take effect the next time the computer is started. The name must not be longer than MAX_COMPUTERNAME_LENGTH characters. 




The standard character set includes letters, numbers, and the following symbols: ! @ # $ % ^ &amp; ' ) ( . - _ { } ~ . If this parameter contains one or more characters that are outside the standard character set, 
<b>SetComputerName</b> returns ERROR_INVALID_PARAMETER. 


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Applications using this function must have administrator rights.




## -see-also




<a href="https://msdn.microsoft.com/7e083cb5-cf0a-4284-8b54-dac856910c44">Computer Names</a>



<a href="https://msdn.microsoft.com/8ca3e611-e5fb-4909-adf6-98eb8552c9e1">GetComputerName</a>



<a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a>



<a href="https://msdn.microsoft.com/12163456-770c-4f9e-9261-a6ea5f2cd93a">SetComputerNameEx</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System Information Functions</a>
 

 


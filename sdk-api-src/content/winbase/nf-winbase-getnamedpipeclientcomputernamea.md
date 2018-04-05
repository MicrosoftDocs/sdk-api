---
UID: NF:winbase.GetNamedPipeClientComputerNameA
title: GetNamedPipeClientComputerNameA function
author: windows-driver-content
description: Retrieves the client computer name for the specified named pipe.
old-location: base\getnamedpipeclientcomputername.htm
old-project: ipc
ms.assetid: 8daa97fe-0ef7-4ada-a99c-aff487ad27e5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetNamedPipeClientComputerName, GetNamedPipeClientComputerName function, GetNamedPipeClientComputerNameA, GetNamedPipeClientComputerNameW, base.getnamedpipeclientcomputername, winbase/GetNamedPipeClientComputerName, winbase/GetNamedPipeClientComputerNameA, winbase/GetNamedPipeClientComputerNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNamedPipeClientComputerNameW (Unicode) and GetNamedPipeClientComputerNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-NamedPipe-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-NamedPipe-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-NamedPipe-l1-2-1.dll
-	API-Ms-Win-Core-Namedpipe-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
-	API-MS-Win-Core-NamedPipe-Ansi-L1-1-1.dll
-	API-MS-Win-Core-NamedPipe-L1-2-2.dll
api_name:
-	GetNamedPipeClientComputerName
-	GetNamedPipeClientComputerNameA
-	GetNamedPipeClientComputerNameW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetNamedPipeClientComputerNameA function


## -description


Retrieves the client computer name for the specified named pipe.


## -parameters




### -param Pipe [in]

A handle to an instance of a named pipe. This handle must be created by the 
<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a> function.


### -param ClientComputerName [out]

The computer name.


### -param ClientComputerNameLength [in]

The size of the <i>ClientComputerName</i> buffer, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax "\\.\pipe\LOCAL\" for the pipe name.




## -see-also




<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a>



<a href="https://msdn.microsoft.com/9e80783e-9641-4cbd-9c28-a8efe6b9efaa">Pipe Functions</a>



<a href="https://msdn.microsoft.com/7cb8cbe4-eec8-4dda-9cb7-8d37abcee6f4">Pipes Overview</a>
 

 


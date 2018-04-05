---
UID: NF:wincon.FreeConsole
title: FreeConsole function
author: windows-driver-content
description: Detaches the calling process from its console.
old-location: consoles\freeconsole.htm
old-project: consoles
ms.assetid: 6c525325-696e-4d8b-8337-cbf9e31c900c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FreeConsole, FreeConsole function [Consoles], _win32_freeconsole, base.freeconsole, consoles.freeconsole, wincon/FreeConsole
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICMetadataPattern
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Console-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
-	FreeConsole
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FreeConsole function


## -description


Detaches the calling process from its console.


## -parameters






## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A process can be attached to at most one console. If the calling process is not already attached to a console, 
the error code returned is <b>ERROR_INVALID_PARAMETER</b> (87).

A process can use the 
<b>FreeConsole</b> function to detach itself from its console. If other processes share the console, the console is not destroyed, but the process that called 
<b>FreeConsole</b> cannot refer to it. A console is closed when the last process attached to it terminates or calls 
<b>FreeConsole</b>. After a process calls <b>FreeConsole</b>, it can call the 
<a href="https://msdn.microsoft.com/bdf3bf2f-8eb8-4ba6-bf3a-a67b29dffda2">AllocConsole</a> function to create a new console or 
<a href="https://msdn.microsoft.com/c00691c3-5878-4a06-9bf3-6073326f36c4">AttachConsole</a> to attach to another console.




## -see-also




<a href="https://msdn.microsoft.com/bdf3bf2f-8eb8-4ba6-bf3a-a67b29dffda2">AllocConsole</a>



<a href="https://msdn.microsoft.com/c00691c3-5878-4a06-9bf3-6073326f36c4">AttachConsole</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/16148ce6-d3be-40dd-b82e-50ea1df67c4e">Consoles</a>
 

 


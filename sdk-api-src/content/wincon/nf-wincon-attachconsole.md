---
UID: NF:wincon.AttachConsole
title: AttachConsole function
author: windows-driver-content
description: Attaches the calling process to the console of the specified process.
old-location: consoles\attachconsole.htm
old-project: consoles
ms.assetid: c00691c3-5878-4a06-9bf3-6073326f36c4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ATTACH_PARENT_PROCESS, AttachConsole, AttachConsole function [Consoles], _win32_attachconsole, base.attachconsole, consoles.attachconsole, wincon/AttachConsole
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
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
-	AttachConsole
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# AttachConsole function


## -description


Attaches the calling process to the console of the specified process.


## -parameters




### -param dwProcessId [in]

The identifier of the process whose console is to be used. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><i>pid</i></dt>
</dl>
</td>
<td width="60%">
Use the console of the specified process.

</td>
</tr>
<tr>
<td width="40%"><a id="ATTACH_PARENT_PROCESS"></a><a id="attach_parent_process"></a><dl>
<dt><b>ATTACH_PARENT_PROCESS</b></dt>
<dt>(DWORD)-1</dt>
</dl>
</td>
<td width="60%">
Use the console of the parent of the current process.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A process can be attached to at most one console. If the calling process is already attached to a console, 
the error code returned is <b>ERROR_ACCESS_DENIED</b> (5). If the specified process does not have a console, the error code returned is <b>ERROR_INVALID_HANDLE</b> (6). If the specified process does not exist, the error code returned is <b>ERROR_INVALID_PARAMETER</b> (87).

A process can use the 
<a href="https://msdn.microsoft.com/6c525325-696e-4d8b-8337-cbf9e31c900c">FreeConsole</a> function to detach itself from its console. If other processes share the console, the console is not destroyed, but the process that called 
<b>FreeConsole</b> cannot refer to it. A console is closed when the last process attached to it terminates or calls 
<b>FreeConsole</b>. After a process calls <b>FreeConsole</b>, it can call the 
<a href="https://msdn.microsoft.com/bdf3bf2f-8eb8-4ba6-bf3a-a67b29dffda2">AllocConsole</a> function to create a new console or 
<b>AttachConsole</b> to attach to another console.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/bdf3bf2f-8eb8-4ba6-bf3a-a67b29dffda2">AllocConsole</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/16148ce6-d3be-40dd-b82e-50ea1df67c4e">Consoles</a>



<a href="https://msdn.microsoft.com/6c525325-696e-4d8b-8337-cbf9e31c900c">FreeConsole</a>



<a href="https://msdn.microsoft.com/3d21103b-662d-4393-ae3f-773cd9e4a930">GetConsoleProcessList</a>
 

 


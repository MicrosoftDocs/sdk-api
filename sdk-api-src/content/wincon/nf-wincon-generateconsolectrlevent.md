---
UID: NF:wincon.GenerateConsoleCtrlEvent
title: GenerateConsoleCtrlEvent function
author: windows-driver-content
description: Sends a specified signal to a console process group that shares the console associated with the calling process.
old-location: consoles\generateconsolectrlevent.htm
old-project: consoles
ms.assetid: ed392d97-6fd0-4256-a783-bc7d27d01a10
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CTRL_BREAK_EVENT, CTRL_C_EVENT, GenerateConsoleCtrlEvent, GenerateConsoleCtrlEvent function [Consoles], _win32_generateconsolectrlevent, base.generateconsolectrlevent, consoles.generateconsolectrlevent, wincon/GenerateConsoleCtrlEvent
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
-	GenerateConsoleCtrlEvent
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GenerateConsoleCtrlEvent function


## -description


Sends a specified signal to a console process group that shares the console associated with the calling process.


## -parameters




### -param dwCtrlEvent [in]

The type of signal to be generated. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CTRL_C_EVENT"></a><a id="ctrl_c_event"></a><dl>
<dt><b>CTRL_C_EVENT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Generates a CTRL+C signal. This signal cannot be generated for process groups. If <i>dwProcessGroupId</i> is nonzero, this function will succeed, but the CTRL+C signal will not be received by processes within the specified process group.

</td>
</tr>
<tr>
<td width="40%"><a id="CTRL_BREAK_EVENT"></a><a id="ctrl_break_event"></a><dl>
<dt><b>CTRL_BREAK_EVENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Generates a CTRL+BREAK signal.

</td>
</tr>
</table>
 


### -param dwProcessGroupId [in]

The identifier of the process group to receive the signal. A process group is created when the <b>CREATE_NEW_PROCESS_GROUP</b> flag is specified in a call to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function. The process identifier of the new process is also the process group identifier of a new process group. The process group includes all processes that are descendants of the root process. Only those processes in the group that share the same console as the calling process receive the signal. In other words, if a process in the group creates a new console, that process does not receive the signal, nor do its descendants. 




If this parameter is zero, the signal is generated in all processes that share the console of the calling process.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GenerateConsoleCtrlEvent</b> causes the control handler functions of processes in the target group to be called. All console processes have a default handler function that calls the 
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a> function. A console process can use the 
<a href="https://msdn.microsoft.com/6fc64265-1403-45ea-925c-c5eb31d56734">SetConsoleCtrlHandler</a> function to install or remove other handler functions.


<a href="https://msdn.microsoft.com/6fc64265-1403-45ea-925c-c5eb31d56734">SetConsoleCtrlHandler</a> can also enable an inheritable attribute that causes the calling process to ignore CTRL+C signals. If 
<b>GenerateConsoleCtrlEvent</b> sends a CTRL+C signal to a process for which this attribute is enabled, the handler functions for that process are not called. CTRL+BREAK signals always cause the handler functions to be called.




## -see-also




<a href="https://msdn.microsoft.com/6480e8ee-d228-4c07-99df-de1e0c3ca250">Console Control Handlers</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>



<a href="https://msdn.microsoft.com/6fc64265-1403-45ea-925c-c5eb31d56734">SetConsoleCtrlHandler</a>
 

 


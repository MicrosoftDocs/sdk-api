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

# WaitForInputIdle function


## -description


Waits until the specified process has finished processing its initial input and is waiting for user input with no input pending, or until the time-out interval has elapsed.


## -parameters




### -param hProcess [in]

A handle to the process. If this process is a console application or does not have a message queue, 
<b>WaitForInputIdle</b> returns immediately.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If <i>dwMilliseconds</i> is INFINITE, the function does not return until the process is idle.


## -returns



The following table shows the possible return values for this function.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The wait was satisfied successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The wait was terminated because the time-out interval elapsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WaitForInputIdle</b> function enables a thread to suspend its execution until the specified process has finished its initialization and is waiting for user input with no input pending. If the process has multiple threads, the <b>WaitForInputIdle</b> function returns as soon as any thread becomes idle. 

<b>WaitForInputIdle</b>  can be used at any time, not just during application startup. However, <b>WaitForInputIdle</b> waits only once for a process to become idle; subsequent <b>WaitForInputIdle</b> calls return immediately, whether the process is idle or busy. 

<b>WaitForInputIdle</b> can be useful for synchronizing a parent process and a newly created child process. When a parent process creates a child process, the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function returns without waiting for the child process to finish its initialization. Before trying to communicate with the child process, the parent process can use 
the <b>WaitForInputIdle</b> function to determine when the child's initialization has been completed. For example, the parent process should use 
the <b>WaitForInputIdle</b> function before trying to find a window associated with the child process.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/74af0502-dae1-438c-8e4b-7663093b3fe3">Synchronizing Execution of Multiple Threads</a>
 

 


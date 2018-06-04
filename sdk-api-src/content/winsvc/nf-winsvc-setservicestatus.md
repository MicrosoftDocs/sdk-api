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

# SetServiceStatus function


## -description


Updates the service control manager's status information for the calling service.


## -parameters




### -param hServiceStatus [in]

A handle to the status information structure for the current service. This handle is returned by the 
<a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a> function.


### -param lpServiceStatus [in]

A pointer to the 
<a href="https://msdn.microsoft.com/d268609b-d442-4d0f-9d49-ed23fee84961">SERVICE_STATUS</a> structure the contains the latest status information for the calling service.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. Other error codes can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The specified service status structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
</table>
 




## -remarks



A 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function first calls the 
<a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a> function to get the service's SERVICE_STATUS_HANDLE. Then it immediately calls the 
<b>SetServiceStatus</b> function to notify the service control manager that its status is SERVICE_START_PENDING. During initialization, the service can provide updated status to indicate that it is making progress but it needs more time. A common bug is for the service to have the main thread perform the initialization while a separate thread continues to call 
<b>SetServiceStatus</b> to prevent the service control manager from marking it as hung. However, if the main thread hangs, then the service start ends up in an infinite loop because the worker thread continues to report that the main thread is making progress.

After processing a control request, the service's 
<a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">Handler</a> function must call 
<b>SetServiceStatus</b> if the service status changes to report its new status to the service control manager. It is only necessary to do so when the service is changing state, such as when it is processing stop or shutdown controls. A service can also use this function at any time from any thread of the service to notify the service control manager of state changes, such as when the service must stop due to a recoverable error.

A service can call this function only after it has called 
<a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a> to get a service status handle.

If a service calls 
<b>SetServiceStatus</b> with the <b>dwCurrentState</b> member set to SERVICE_STOPPED and the <b>dwWin32ExitCode</b> member set to a nonzero value, the following entry is written into the System event log:

<pre class="syntax" xml:space="preserve"><code>   Event ID    = 7023
   Source      = Service Control Manager
   Type        = Error
   Description = &lt;ServiceName&gt; terminated with the following error:
                 &lt;ExitCode&gt;.</code></pre>
The following are best practices when calling this function:

<ul>
<li>Initialize all fields in the <a href="https://msdn.microsoft.com/d268609b-d442-4d0f-9d49-ed23fee84961">SERVICE_STATUS</a> structure, ensuring that there are valid check-point and wait hint values for pending states. Use reasonable wait hints.</li>
<li>Do not register to accept controls while the status is SERVICE_START_PENDING or the service can crash. After initialization is completed, accept the SERVICE_CONTROL_STOP code.</li>
<li>Call this function with checkpoint and wait-hint values only if the service is making progress on the tasks related to the pending start, stop, pause, or continue operation. Otherwise, SCM cannot detect if your service is hung.</li>
<li>Enter the stopped state with an appropriate exit code if <a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> fails.</li>
<li>If the status is SERVICE_STOPPED, perform all necessary cleanup and call <b>SetServiceStatus</b> one time only. This function makes an LRPC call to the SCM. The first call to the function in the SERVICE_STOPPED state closes the RPC context handle and any subsequent calls can cause the process to crash. </li>
<li>Do not attempt to perform any additional work after calling <b>SetServiceStatus</b> with SERVICE_STOPPED, because the service process can be terminated at any time.</li>
</ul>

#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7aa9371d-676c-4633-9831-edf0e74d15f0">Writing a ServiceMain Function</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a>



<a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a>



<a href="https://msdn.microsoft.com/d268609b-d442-4d0f-9d49-ed23fee84961">SERVICE_STATUS</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a>



<a href="https://msdn.microsoft.com/91a985d4-d1af-4161-ae67-a8a9d6740838">SetServiceBits</a>
 

 


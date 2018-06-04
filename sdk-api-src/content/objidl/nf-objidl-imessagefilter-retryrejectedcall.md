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

# IMessageFilter::RetryRejectedCall


## -description


Provides applications with an opportunity to display a dialog box offering retry, cancel, or task-switching options.


## -parameters




### -param htaskCallee [in]

The thread id of the called application.


### -param dwTickCount [in]

The number of elapsed ticks since the call was made.


### -param dwRejectType [in]

Specifies either SERVERCALL_REJECTED or SERVERCALL_RETRYLATER, as returned by the object application.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The call should be canceled. COM then returns RPC_E_CALL_REJECTED from the original method call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0 ≤ <i>value</i> &lt; 100</dt>
</dl>
</td>
<td width="60%">
The call is to be retried immediately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>100 ≤ <i>value</i> </dt>
</dl>
</td>
<td width="60%">
COM will wait for this many milliseconds and then retry the call.

</td>
</tr>
</table>
 




## -remarks



COM calls <b>RetryRejectedCall</b> on the caller's <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a> interface immediately after receiving SERVERCALL_RETRYLATER or SERVERCALL_REJECTED from the <a href="https://msdn.microsoft.com/7e31b518-ef4f-4bdd-b5c7-e1b16383a5be">IMessageFilter::HandleInComingCall</a> method on the callee's <b>IMessageFilter</b> interface.

If a called task rejects a call, the application is probably in a state where it cannot handle such calls, possibly only temporarily. When this occurs, COM returns to the caller and issues <b>RetryRejectedCall</b> to determine whether it should retry the rejected call.

Applications should silently retry calls that have returned with SERVERCALL_RETRYLATER. If, after a reasonable amount of time has passed, say about 30 seconds, the application should display the busy dialog box; a standard implementation of this dialog box is available in the OLEDLG library. The callee may momentarily be in a state where calls can be handled. The option to wait and retry is provided for special kinds of calling applications, such as background tasks executing macros or scripts, so that they can retry the calls in a nonintrusive way.

If, after a dialog box is displayed, the user chooses to cancel, <b>RetryRejectedCall</b> returns -1 and the call will appear to fail with RPC_E_CALL_REJECTED.

If a client implements <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a> and calls a server method on a remote machine, <b>RetryRejectedCall</b> will not be called.

<div class="alert"><b>Note</b>  Although the <i>htaskCallee</i> parameter is typed as an HTASK, it  contains the thread id of the called thread. When you implement the <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a> interface, you can call the <a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a> function to get the thread handle from the <i>htaskCallee</i> parameter,  and you can call the <a href="https://msdn.microsoft.com/1878088b-e0fd-4009-b608-f491805948b5">GetProcessIdOfThread</a> function to get the process id.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a>
 

 


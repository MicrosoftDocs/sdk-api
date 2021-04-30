---
UID: NF:objidl.IMessageFilter.RetryRejectedCall
title: IMessageFilter::RetryRejectedCall (objidl.h)
description: Provides applications with an opportunity to display a dialog box offering retry, cancel, or task-switching options.
helpviewer_keywords: ["IMessageFilter interface [COM]","RetryRejectedCall method","IMessageFilter.RetryRejectedCall","IMessageFilter::RetryRejectedCall","RetryRejectedCall","RetryRejectedCall method [COM]","RetryRejectedCall method [COM]","IMessageFilter interface","_com_imessagefilter_retryrejectedcall","com.imessagefilter_retryrejectedcall","objidl/IMessageFilter::RetryRejectedCall"]
old-location: com\imessagefilter_retryrejectedcall.htm
tech.root: com
ms.assetid: 3f800819-2a21-4e46-ad15-f9594fac1a3d
ms.date: 12/05/2018
ms.keywords: IMessageFilter interface [COM],RetryRejectedCall method, IMessageFilter.RetryRejectedCall, IMessageFilter::RetryRejectedCall, RetryRejectedCall, RetryRejectedCall method [COM], RetryRejectedCall method [COM],IMessageFilter interface, _com_imessagefilter_retryrejectedcall, com.imessagefilter_retryrejectedcall, objidl/IMessageFilter::RetryRejectedCall
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMessageFilter::RetryRejectedCall
 - objidl/IMessageFilter::RetryRejectedCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMessageFilter.RetryRejectedCall
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

COM calls <b>RetryRejectedCall</b> on the caller's <a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a> interface immediately after receiving SERVERCALL_RETRYLATER or SERVERCALL_REJECTED from the <a href="/windows/desktop/api/objidl/nf-objidl-imessagefilter-handleincomingcall">IMessageFilter::HandleInComingCall</a> method on the callee's <b>IMessageFilter</b> interface.

If a called task rejects a call, the application is probably in a state where it cannot handle such calls, possibly only temporarily. When this occurs, COM returns to the caller and issues <b>RetryRejectedCall</b> to determine whether it should retry the rejected call.

Applications should silently retry calls that have returned with SERVERCALL_RETRYLATER. If, after a reasonable amount of time has passed, say about 30 seconds, the application should display the busy dialog box; a standard implementation of this dialog box is available in the OLEDLG library. The callee may momentarily be in a state where calls can be handled. The option to wait and retry is provided for special kinds of calling applications, such as background tasks executing macros or scripts, so that they can retry the calls in a nonintrusive way.

If, after a dialog box is displayed, the user chooses to cancel, <b>RetryRejectedCall</b> returns -1 and the call will appear to fail with RPC_E_CALL_REJECTED.

If a client implements <a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a> and calls a server method on a remote machine, <b>RetryRejectedCall</b> will not be called.

<div class="alert"><b>Note</b>  Although the <i>htaskCallee</i> parameter is typed as an HTASK, it  contains the thread id of the called thread. When you implement the <a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a> interface, you can call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a> function to get the thread handle from the <i>htaskCallee</i> parameter,  and you can call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread">GetProcessIdOfThread</a> function to get the process id.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a>
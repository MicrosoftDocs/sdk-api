---
UID: NF:objidl.IMessageFilter.MessagePending
title: IMessageFilter::MessagePending (objidl.h)
description: Indicates that a message has arrived while COM is waiting to respond to a remote call.
helpviewer_keywords: ["IMessageFilter interface [COM]","MessagePending method","IMessageFilter.MessagePending","IMessageFilter::MessagePending","MessagePending","MessagePending method [COM]","MessagePending method [COM]","IMessageFilter interface","_com_imessagefilter_messagepending","com.imessagefilter_messagepending","objidl/IMessageFilter::MessagePending"]
old-location: com\imessagefilter_messagepending.htm
tech.root: com
ms.assetid: f4aff53f-c344-4456-b53e-296d5a5b653a
ms.date: 12/05/2018
ms.keywords: IMessageFilter interface [COM],MessagePending method, IMessageFilter.MessagePending, IMessageFilter::MessagePending, MessagePending, MessagePending method [COM], MessagePending method [COM],IMessageFilter interface, _com_imessagefilter_messagepending, com.imessagefilter_messagepending, objidl/IMessageFilter::MessagePending
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
 - IMessageFilter::MessagePending
 - objidl/IMessageFilter::MessagePending
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
 - IMessageFilter.MessagePending
---

# IMessageFilter::MessagePending


## -description

Indicates that a message has arrived while COM is waiting to respond to a remote call.

Handling input while waiting for an outgoing call to finish can introduce complications. The application should determine whether to process the message without interrupting the call, to continue waiting, or to cancel the operation.

## -parameters

### -param htaskCallee [in]

The thread id of the called application.

### -param dwTickCount [in]

The number of ticks since the call was made. It is calculated from the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount">GetTickCount</a> function.

### -param dwPendingType [in]

The type of call made during which a message or event was received. Possible values are from the enumeration <a href="/windows/desktop/api/objidl/ne-objidl-pendingtype">PENDINGTYPE</a>, where PENDINGTYPE_TOPLEVEL means the outgoing call was not nested within a call from another application and PENDINTGYPE_NESTED means the outgoing call was nested within a call from another application.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PENDINGMSG_CANCELCALL</b></dt>
</dl>
</td>
<td width="60%">
Cancel the outgoing call. This should be returned only under extreme conditions. Canceling a call that has not replied or been rejected can create orphan transactions and lose resources. COM fails the original call and returns RPC_E_CALL_CANCELLED.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PENDINGMSG_WAITNOPROCESS</b></dt>
</dl>
</td>
<td width="60%">
Unused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PENDINGMSG_WAITDEFPROCESS</b></dt>
</dl>
</td>
<td width="60%">
Keyboard and mouse messages are no longer dispatched. However there are some cases where mouse and keyboard messages could cause the system to deadlock, and in these cases, mouse and keyboard messages are discarded. WM_PAINT messages are dispatched. Task-switching and activation messages are handled as before.

</td>
</tr>
</table>

## -remarks

COM calls <b>MessagePending</b> after an application has made a COM method call and a Windows message occurs before the call has returned. A Windows message is sent, for example, when the user selects a menu command or double-clicks an object. Before COM makes the <b>MessagePending</b> call, it calculates the elapsed time since the original COM method call was made. COM delivers the elapsed time in the <i>dwTickCount</i> parameter. In the meantime, COM does not remove the message from the queue.

Windows messages that appear in the caller's queue should remain in the queue until sufficient time has passed to ensure that the messages are probably not the result of typing ahead, but are instead an attempt to get attention. Set the delay with the <i>dwTickCount</i> parameter —a two-second or three-second delay is recommended. If that amount of time passes and the call has not been completed, the caller should flush the messages from the queue and the OLE UI busy dialog box should be displayed offering the user the choice of retrying the call (continue waiting) or switching to the specified task. This ensures the following behaviors:

<ul>
<li>
If calls are completed in a reasonable amount of time, type ahead will be treated correctly.

</li>
<li>
If the callee does not respond, type ahead is not misinterpreted and the user is able to act to solve the problem. For example, OLE 1 servers can queue up requests without responding when they are in modal dialog boxes.

</li>
</ul>
Handling input while waiting for an outgoing call to finish can introduce complications. The application should determine whether to process the message without interrupting the call, to continue waiting, or to cancel the operation.

When there is no response to the original COM call, the application can cancel the call and restore the COM object to a consistent state by calling <a href="/windows/desktop/api/objidl/nf-objidl-istorage-revert">IStorage::Revert</a> on its storage. The object can be released when the container can shut down. However, canceling a call can create orphaned operations and resource leaks. Canceling should be used only as a last resort. It is strongly recommended that applications not allow such calls to be canceled.

<div class="alert"><b>Note</b>  Although the <i>htaskCallee</i> parameter is typed as an HTASK, it  contains the thread id of the called thread. When you implement the <a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a> interface, you can call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a> function to get the thread handle from the <i>htaskCallee</i> parameter,  and you can call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread">GetProcessIdOfThread</a> function to get the process id.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuibusya">OleUIBusy</a>
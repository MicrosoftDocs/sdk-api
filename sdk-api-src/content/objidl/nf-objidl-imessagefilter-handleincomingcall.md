---
UID: NF:objidl.IMessageFilter.HandleInComingCall
title: IMessageFilter::HandleInComingCall (objidl.h)
description: Provides a single entry point for incoming calls.
helpviewer_keywords: ["HandleInComingCall","HandleInComingCall method [COM]","HandleInComingCall method [COM]","IMessageFilter interface","IMessageFilter interface [COM]","HandleInComingCall method","IMessageFilter.HandleInComingCall","IMessageFilter::HandleInComingCall","_com_imessagefilter_handleincomingcall","com.imessagefilter_handleincomingcall","objidl/IMessageFilter::HandleInComingCall"]
old-location: com\imessagefilter_handleincomingcall.htm
tech.root: com
ms.assetid: 7e31b518-ef4f-4bdd-b5c7-e1b16383a5be
ms.date: 12/05/2018
ms.keywords: HandleInComingCall, HandleInComingCall method [COM], HandleInComingCall method [COM],IMessageFilter interface, IMessageFilter interface [COM],HandleInComingCall method, IMessageFilter.HandleInComingCall, IMessageFilter::HandleInComingCall, _com_imessagefilter_handleincomingcall, com.imessagefilter_handleincomingcall, objidl/IMessageFilter::HandleInComingCall
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
 - IMessageFilter::HandleInComingCall
 - objidl/IMessageFilter::HandleInComingCall
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
 - IMessageFilter.HandleInComingCall
---

# IMessageFilter::HandleInComingCall


## -description

Provides a single entry point for incoming calls.

This method is called prior to each method invocation originating outside the current process and provides the ability to filter or reject incoming calls (or callbacks) to an object or a process.

## -parameters

### -param dwCallType [in]

The type of incoming call that has been received. Possible values are from the enumeration <a href="/windows/desktop/api/objidl/ne-objidl-calltype">CALLTYPE</a>.

### -param htaskCaller [in]

The thread id of the caller.

### -param dwTickCount [in]

The elapsed tick count since the outgoing call was made, if <i>dwCallType</i> is not CALLTYPE_TOPLEVEL. If <i>dwCallType</i> is CALLTYPE_TOPLEVEL, <i>dwTickCount</i> should be ignored.

### -param lpInterfaceInfo [in]

A pointer to an <a href="/windows/desktop/api/objidl/ns-objidl-interfaceinfo">INTERFACEINFO</a> structure that identifies the object, interface, and method being called. In the case of DDE calls, <i>lpInterfaceInfo</i> can be <b>NULL</b> because the DDE layer does not return interface information.

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
<dt><b>SERVERCALL_ISHANDLED</b></dt>
</dl>
</td>
<td width="60%">
The application might be able to process the call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SERVERCALL_REJECTED</b></dt>
</dl>
</td>
<td width="60%">
The application cannot handle the call due to an unforeseen problem, such as network unavailability, or if it is in the process of terminating.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SERVERCALL_RETRYLATER</b></dt>
</dl>
</td>
<td width="60%">
The application cannot handle the call at this time. An application might return this value when it is in a user-controlled modal state.

</td>
</tr>
</table>

## -remarks

If implemented, <b>HandleInComingCall</b> is called by COM when an incoming COM message is received.

Depending on an application's current state, a call is either accepted and processed or rejected (permanently or temporarily). If SERVERCALL_ISHANDLED is returned, the application may be able to process the call, although success depends on the interface for which the call is destined. If the call cannot be processed, COM returns RPC_E_CALL_REJECTED.

Input-synchronized and asynchronous calls are dispatched even if the application returns SERVERCALL_REJECTED or SERVERCALL_RETRYLATER.

<b>HandleInComingCall</b> should not be used to hold off updates to objects during operations such as band printing. For that purpose, use <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-freeze">IViewObject::Freeze</a>.

You can also use <b>HandleInComingCall</b> to set up the application's state so that the call can be processed in the future.

<div class="alert"><b>Note</b>  Although the <i>htaskCaller</i> parameter is typed as an HTASK, it  contains the thread id of the calling thread. When you implement the <a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a> interface, you can call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a> function to get the thread handle from the <i>htaskCaller</i> parameter,  and you can call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread">GetProcessIdOfThread</a> function to get the process id.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a>
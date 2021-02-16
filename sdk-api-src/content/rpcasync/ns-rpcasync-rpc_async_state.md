---
UID: NS:rpcasync._RPC_ASYNC_STATE
title: RPC_ASYNC_STATE (rpcasync.h)
description: The RPC_ASYNC_STATE structure holds the state of an asynchronous remote procedure call. RPC_ASYNC_STATE is a handle to this structure, used to wait for, query, reply to, or cancel asynchronous calls.
helpviewer_keywords: ["*PRPC_ASYNC_STATE","PRPC_ASYNC_STATE","PRPC_ASYNC_STATE structure pointer [RPC]","RPC_ASYNC_STATE","RPC_ASYNC_STATE structure [RPC]","RPC_C_NOTIFY_ON_SEND_COMPLETE","RpcNotificationTypeApc","RpcNotificationTypeCallback","RpcNotificationTypeEvent","RpcNotificationTypeHwnd","RpcNotificationTypeIoc","RpcNotificationTypeNone","_rpc_rpc_async_state","rpc.rpc_async_state","rpcasync/PRPC_ASYNC_STATE","rpcasync/RPC_ASYNC_STATE"]
old-location: rpc\rpc_async_state.htm
tech.root: Rpc
ms.assetid: ad004f49-89a6-486c-80ec-5b85ab4b8db9
ms.date: 12/05/2018
ms.keywords: '*PRPC_ASYNC_STATE, PRPC_ASYNC_STATE, PRPC_ASYNC_STATE structure pointer [RPC], RPC_ASYNC_STATE, RPC_ASYNC_STATE structure [RPC], RPC_C_NOTIFY_ON_SEND_COMPLETE, RpcNotificationTypeApc, RpcNotificationTypeCallback, RpcNotificationTypeEvent, RpcNotificationTypeHwnd, RpcNotificationTypeIoc, RpcNotificationTypeNone, _rpc_rpc_async_state, rpc.rpc_async_state, rpcasync/PRPC_ASYNC_STATE, rpcasync/RPC_ASYNC_STATE'
req.header: rpcasync.h
req.include-header: Rpc.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_ASYNC_STATE, *PRPC_ASYNC_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_ASYNC_STATE
 - rpcasync/_RPC_ASYNC_STATE
 - PRPC_ASYNC_STATE
 - rpcasync/PRPC_ASYNC_STATE
 - RPC_ASYNC_STATE
 - rpcasync/RPC_ASYNC_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RPC_ASYNC_STATE
---

# RPC_ASYNC_STATE structure


## -description

The 
<b>RPC_ASYNC_STATE</b> structure holds the state of an asynchronous remote procedure call. <b>RPC_ASYNC_STATE</b> is a handle to this structure, used to wait for, query, reply to, or cancel asynchronous calls.

## -struct-fields

### -field Size

Size of this structure, in bytes. The environment sets this member when 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a> is called. Do not modify this member.

### -field Signature

The run-time environment sets this member when 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a> is called. Do not modify this member.

### -field Lock

The run-time environment sets this member when 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a> is called. Do not modify this member.

### -field Flags

The <b>flags</b> member can be set to the following values. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_NOTIFY_ON_SEND_COMPLETE"></a><a id="rpc_c_notify_on_send_complete"></a><dl>
<dt><b>RPC_C_NOTIFY_ON_SEND_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Posts a notification message when the asynchronous operation is complete.

</td>
</tr>
</table>
 

These flags are used with DCE pipes, which allow applications to send or receive data in multiple blocks. Programs can either send a continuous stream of data or wait for each block to be transmitted before it sends the next block. If it does not wait, the RPC run-time library will buffer the output until it can be sent. When the data transmission is complete, the RPC library sends the application a notification. If an application specifies the RPC_C_NOTIFY_ON_SEND_COMPLETE flag, the RPC library sends it a member of the 
<a href="/windows/desktop/api/rpcasync/ne-rpcasync-rpc_notification_types">RPC_NOTIFICATION_TYPES</a> enumeration after it completes each send operation.

### -field StubInfo

Reserved for use by the stubs. Do not use this member.

### -field UserInfo

Use this member for any application-specific information that you want to keep track of in this structure.

### -field RuntimeInfo

Reserved for use by the RPC run-time environment. Do not use this member.

### -field Event

Type of event that occurred. The RPC run-time environment sets this field to a member of the 
<a href="/windows/desktop/api/rpcasync/ne-rpcasync-rpc_async_event">RPC_ASYNC_EVENT</a> enumeration.

### -field NotificationType

Type of notification the RPC run time should use to notify the client for the occurrence of an event, such as completion of the call or completion of the event.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RpcNotificationTypeNone"></a><a id="rpcnotificationtypenone"></a><a id="RPCNOTIFICATIONTYPENONE"></a><dl>
<dt><b>RpcNotificationTypeNone</b></dt>
</dl>
</td>
<td width="60%">
No notification is specified; <a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_notification_info">RPC_ASYNC_NOTIFICATION_INFO</a> is not initialized.

</td>
</tr>
<tr>
<td width="40%"><a id="RpcNotificationTypeEvent"></a><a id="rpcnotificationtypeevent"></a><a id="RPCNOTIFICATIONTYPEEVENT"></a><dl>
<dt><b>RpcNotificationTypeEvent</b></dt>
</dl>
</td>
<td width="60%">
The notification mechanism is a Windows event.

</td>
</tr>
<tr>
<td width="40%"><a id="RpcNotificationTypeApc"></a><a id="rpcnotificationtypeapc"></a><a id="RPCNOTIFICATIONTYPEAPC"></a><dl>
<dt><b>RpcNotificationTypeApc</b></dt>
</dl>
</td>
<td width="60%">
The notification mechanism is a Windows asynchronous procedure call.

</td>
</tr>
<tr>
<td width="40%"><a id="RpcNotificationTypeIoc"></a><a id="rpcnotificationtypeioc"></a><a id="RPCNOTIFICATIONTYPEIOC"></a><dl>
<dt><b>RpcNotificationTypeIoc</b></dt>
</dl>
</td>
<td width="60%">
The notification mechanism is an I/O completion port.

</td>
</tr>
<tr>
<td width="40%"><a id="RpcNotificationTypeHwnd"></a><a id="rpcnotificationtypehwnd"></a><a id="RPCNOTIFICATIONTYPEHWND"></a><dl>
<dt><b>RpcNotificationTypeHwnd</b></dt>
</dl>
</td>
<td width="60%">
The notification mechanism is a Windows system message.

<b>Windows Server 2003 or later:  </b>Notification via the HWND is deprecated. Do not use this value.

</td>
</tr>
<tr>
<td width="40%"><a id="RpcNotificationTypeCallback"></a><a id="rpcnotificationtypecallback"></a><a id="RPCNOTIFICATIONTYPECALLBACK"></a><dl>
<dt><b>RpcNotificationTypeCallback</b></dt>
</dl>
</td>
<td width="60%">
The notification mechanism is a function callback.

</td>
</tr>
</table>

### -field u

Contains asynchronous notification information formatted for the mechanism type specified in <b>NotificationType</b>. 

<div class="alert"><b>Note</b>  Previous to Windows Vista, this member contained the specific syntax of the union currently specified by the <a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_notification_info">RPC_ASYNC_NOTIFICATION_INFO</a> union.</div>
<div> </div>

### -field Reserved

Reserved for compatibility with future versions, if any. Do not use this member.

## -remarks

The client allocates space for the 
<b>RPC_ASYNC_STATE</b> structure and an associated handle, and calls 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a> to initialize the structure. After the run-time environment has successfully initialized the structure, the client initializes the <b>NotificationType</b>, and exactly one of the following structures in the <a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_notification_info">RPC_ASYNC_NOTIFICATION_INFO</a> union: <b>APC</b> for a Windows asynchronous procedure call, <b>IOC</b> for an I/O completion port, <b>HWND</b> for a Windows system message, or <b>hEvent</b> for a Windows event. If the chosen notification method is <b>RpcNotificationTypeNone</b>, no field of the union needs to be initialized. The RPC client may optionally initialize the <b>UserInfo</b> field as well.

## -see-also

<a href="/windows/desktop/Rpc/asynchronous-rpc">Asynchronous RPC</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncabortcall">RpcAsyncAbortCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccancelcall">RpcAsyncCancelCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasynccompletecall">RpcAsyncCompleteCall</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallstatus">RpcAsyncGetCallStatus</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncinitializehandle">RpcAsyncInitializeHandle</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcservertestcancel">RpcServerTestCancel</a>
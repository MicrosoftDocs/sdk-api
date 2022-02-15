---
UID: NE:tapi3if.CALL_STATE
title: CALL_STATE (tapi3if.h)
description: The CALL_STATE enum is used by the ITCallInfo::get_CallState and ITCallStateEvent::get_State methods.
helpviewer_keywords: ["CALL_STATE","CALL_STATE enumeration [TAPI 2.2]","CS_CONNECTED","CS_DISCONNECTED","CS_HOLD","CS_IDLE","CS_INPROGRESS","CS_OFFERING","CS_QUEUED","_tapi3_call_state","tapi3.call_state","tapi3if/CALL_STATE","tapi3if/CS_CONNECTED","tapi3if/CS_DISCONNECTED","tapi3if/CS_HOLD","tapi3if/CS_IDLE","tapi3if/CS_INPROGRESS","tapi3if/CS_OFFERING","tapi3if/CS_QUEUED"]
old-location: tapi3\call_state.htm
tech.root: tapi3
ms.assetid: d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1
ms.date: 12/05/2018
ms.keywords: CALL_STATE, CALL_STATE enumeration [TAPI 2.2], CS_CONNECTED, CS_DISCONNECTED, CS_HOLD, CS_IDLE, CS_INPROGRESS, CS_OFFERING, CS_QUEUED, _tapi3_call_state, tapi3.call_state, tapi3if/CALL_STATE, tapi3if/CS_CONNECTED, tapi3if/CS_DISCONNECTED, tapi3if/CS_HOLD, tapi3if/CS_IDLE, tapi3if/CS_INPROGRESS, tapi3if/CS_OFFERING, tapi3if/CS_QUEUED
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CALL_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALL_STATE
 - tapi3if/CALL_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALL_STATE
---

# CALL_STATE enumeration


## -description

The 
<b>CALL_STATE</b> enum is used by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callstate">ITCallInfo::get_CallState</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallstateevent-get_state">ITCallStateEvent::get_State</a> methods.

## -enum-fields

### -field CS_IDLE:0

The call has been created, but 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect">Connect</a> has not been called yet. A call can never transition into the idle state. This is the initial state for both incoming and outgoing calls.

### -field CS_INPROGRESS

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect">Connect</a> has been called, and the service provider is working on making a connection. This state is valid only on outgoing calls. This message is optional, because a service provider may have a call transition directly to the connected state.

### -field CS_CONNECTED

Call has been connected to the remote end and communication can take place.

### -field CS_DISCONNECTED

Call has been disconnected. There are several causes for disconnection. See the table of valid call state transitions below.

### -field CS_OFFERING

A new call has appeared, and is being offered to an application. If the application has owner privileges on the call, it can either call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer">Answer</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">Disconnect</a> while the call is in the offering state. Current call privilege can be determined by calling 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege">ITCallInfo::get_Privilege</a>.

### -field CS_HOLD

The call is in the hold state.

### -field CS_QUEUED

The call is queued.

### -field CS_LASTITEM:CS_QUEUED

## -remarks

Following is a table of all valid call state transitions.

<table>
<tr>
<th>From state</th>
<th>To state</th>
</tr>
<tr>
<td>CS_IDLE</td>
<td>
<dl>
<dt>INPROGRESS</dt>
<dt>CONNECTED</dt>
<dt>DISCONNECTED</dt>
<dt>OFFERING</dt>
<dt>HOLD</dt>
</dl>
</td>
</tr>
<tr>
<td>CS_INPROGRESS</td>
<td>
<dl>
<dt>CONNECTED</dt>
<dt>DISCONNECTED</dt>
<dt>HOLD</dt>
</dl>
</td>
</tr>
<tr>
<td>CS_CONNECTED</td>
<td>
<dl>
<dt>HOLD</dt>
<dt>DISCONNECTED</dt>
</dl>
</td>
</tr>
<tr>
<td>CS_DISCONNECTED</td>
<td>Nothing—call should be freed</td>
</tr>
<tr>
<td>CS_OFFERING</td>
<td>
<dl>
<dt>CONNECTED</dt>
<dt>DISCONNECTED</dt>
<dt>HOLD</dt>
</dl>
</td>
</tr>
<tr>
<td>CS_HOLD</td>
<td>
<dl>
<dt>CONNECTED</dt>
<dt>DISCONNECTED</dt>
</dl>
</td>
</tr>
<tr>
<td>CS_QUEUED</td>
<td>
<dl>
<dt>CONNECTED</dt>
<dt>DISCONNECTED</dt>
<dt>HOLD</dt>
</dl>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callstate">ITCallInfo::get_CallState</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallstateevent-get_state">ITCallStateEvent::get_State</a>

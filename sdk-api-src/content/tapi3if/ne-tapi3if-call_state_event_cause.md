---
UID: NE:tapi3if.CALL_STATE_EVENT_CAUSE
title: CALL_STATE_EVENT_CAUSE (tapi3if.h)
description: The CALL_STATE_EVENT_CAUSE enum is returned by the ITCallStateEvent::get_Cause method.
helpviewer_keywords: ["CALL_STATE_EVENT_CAUSE","CALL_STATE_EVENT_CAUSE enumeration [TAPI 2.2]","CEC_DISCONNECT_BADADDRESS","CEC_DISCONNECT_BUSY","CEC_DISCONNECT_CANCELLED","CEC_DISCONNECT_FAILED","CEC_DISCONNECT_NOANSWER","CEC_DISCONNECT_NORMAL","CEC_DISCONNECT_REJECTED","CEC_NONE","_tapi3_call_state_event_cause","tapi3.call_state_event_cause","tapi3if/CALL_STATE_EVENT_CAUSE","tapi3if/CEC_DISCONNECT_BADADDRESS","tapi3if/CEC_DISCONNECT_BUSY","tapi3if/CEC_DISCONNECT_CANCELLED","tapi3if/CEC_DISCONNECT_FAILED","tapi3if/CEC_DISCONNECT_NOANSWER","tapi3if/CEC_DISCONNECT_NORMAL","tapi3if/CEC_DISCONNECT_REJECTED","tapi3if/CEC_NONE"]
old-location: tapi3\call_state_event_cause.htm
tech.root: tapi3
ms.assetid: 9bc9e050-41f7-4330-a263-db745d3fa3f8
ms.date: 12/05/2018
ms.keywords: CALL_STATE_EVENT_CAUSE, CALL_STATE_EVENT_CAUSE enumeration [TAPI 2.2], CEC_DISCONNECT_BADADDRESS, CEC_DISCONNECT_BUSY, CEC_DISCONNECT_CANCELLED, CEC_DISCONNECT_FAILED, CEC_DISCONNECT_NOANSWER, CEC_DISCONNECT_NORMAL, CEC_DISCONNECT_REJECTED, CEC_NONE, _tapi3_call_state_event_cause, tapi3.call_state_event_cause, tapi3if/CALL_STATE_EVENT_CAUSE, tapi3if/CEC_DISCONNECT_BADADDRESS, tapi3if/CEC_DISCONNECT_BUSY, tapi3if/CEC_DISCONNECT_CANCELLED, tapi3if/CEC_DISCONNECT_FAILED, tapi3if/CEC_DISCONNECT_NOANSWER, tapi3if/CEC_DISCONNECT_NORMAL, tapi3if/CEC_DISCONNECT_REJECTED, tapi3if/CEC_NONE
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
req.typenames: CALL_STATE_EVENT_CAUSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALL_STATE_EVENT_CAUSE
 - tapi3if/CALL_STATE_EVENT_CAUSE
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
 - CALL_STATE_EVENT_CAUSE
---

# CALL_STATE_EVENT_CAUSE enumeration


## -description

The 
<b>CALL_STATE_EVENT_CAUSE</b> enum is returned by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallstateevent-get_cause">ITCallStateEvent::get_Cause</a> method.

## -enum-fields

### -field CEC_NONE:0

No call event has occurred.

### -field CEC_DISCONNECT_NORMAL

The call was disconnected as part of the normal life cycle of the call (that is, the call was over, so it was disconnected).

### -field CEC_DISCONNECT_BUSY

An outgoing call failed to connect because the remote end was busy.

### -field CEC_DISCONNECT_BADADDRESS

An outgoing call failed because the destination address was bad.

### -field CEC_DISCONNECT_NOANSWER

An outgoing call failed because the remote end was not answered.

### -field CEC_DISCONNECT_CANCELLED

An outgoing call failed because the caller disconnected.

### -field CEC_DISCONNECT_REJECTED

The outgoing call was rejected by the remote end.

### -field CEC_DISCONNECT_FAILED

The call failed to connect for some other reason.

### -field CEC_DISCONNECT_BLOCKED

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallstateevent-get_cause">ITCallStateEvent::get_Cause</a>

---
UID: NF:fwpmu.FwpmNetEventSubscribe3
title: FwpmNetEventSubscribe3
description: Used to request the delivery of notifications regarding a particular net event.
tech.root: fwp
ms.date: 05/01/2024
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Fwpuclnt.dll
req.header: fwpmu.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Fwpuclnt.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmNetEventSubscribe3
f1_keywords:
 - FwpmNetEventSubscribe3
 - fwpmu/FwpmNetEventSubscribe3
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmNetEventSubscribe3
---

## -description

Used to request the delivery of notifications regarding a particular net event.

## -parameters

### -param engineHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an open session with the filter engine. To open a session with the filter engine, call [FwpmEngineOpen0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineopen0).

### -param subscription

An [FWPM_NET_EVENT_SUBSCRIPTION0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0) structure that describes which notifications will be delivered.

### -param callback

Pointer to a function of type [FWPM_NET_EVENT_CALLBACK3](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_net_event_callback3), which will be invoked when a notification is ready for delivery.

### -param context

Optional context pointer. This pointer is passed to the *callback* function along with details of the event.

### -param eventsHandle

Handle to the newly created subscription. Call [FwpmNetEventUnsubscribe0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmneteventunsubscribe0) to close this handle when the subscription is no longer needed.

## -returns

|Return code/value|Description|
|-|-|
|ERROR_SUCCESS<br/>0|The subscription was created successfully.|
|FWP_E_* error code<br/>0x80320001—0x80320039|A Windows Filtering Platform (WFP)-specific error. For details, see [WFP error codes](/windows/win32/fwp/wfp-error-codes).|
|RPC_* error code<br/>0x80010001—0x80010122|Failure to communicate with the remote or local firewall engine.|

## -remarks

You can't call this function within a transaction. It will fail with **FWP_E_TXN_IN_PROGRESS**. For more info about transactions, see [Object management](/windows/win32/fwp/object-management).

To call this function, you need [FWPM_ACTRL_SUBSCRIBE](/windows/win32/fwp/access-right-identifiers) access to the net event's container.

## -see-also

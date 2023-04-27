---
UID: NF:fwpmu.FwpmNetEventSubscribe0
title: FwpmNetEventSubscribe0 function (fwpmu.h)
description: Is used to request the delivery of notifications regarding a particular net event. (FwpmNetEventSubscribe0)
helpviewer_keywords: ["FwpmNetEventSubscribe0","FwpmNetEventSubscribe0 function [Filtering]","fwp.fwpmneteventsubscribe0","fwpmu/FwpmNetEventSubscribe0"]
old-location: fwp\fwpmneteventsubscribe0.htm
tech.root: fwp
ms.assetid: a2671600-c231-46c8-966d-f444fbdfa944
ms.date: 12/05/2018
ms.keywords: FwpmNetEventSubscribe0, FwpmNetEventSubscribe0 function [Filtering], fwp.fwpmneteventsubscribe0, fwpmu/FwpmNetEventSubscribe0
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmNetEventSubscribe0
 - fwpmu/FwpmNetEventSubscribe0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmNetEventSubscribe0
---

# FwpmNetEventSubscribe0 function


## -description

The <b>FwpmNetEventSubscribe0</b> function  is used to request the delivery of notifications regarding a particular net event.
<div class="alert"><b>Note</b>  <b>FwpmNetEventSubscribe0</b> is the specific implementation of FwpmNetEventSubscribe used in Windows 7. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1">FwpmNetEventSubscribe1</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param subscription [in]

Type: [FWPM_NET_EVENT_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)*</b>

The notifications which will be delivered.

### -param callback [in]

Type: <b><a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback0">FWPM_NET_EVENT_CALLBACK0</a></b>

Function pointer that will be invoked when a notification is ready for delivery.

### -param context [in, optional]

Type: <b>void*</b>

Optional context pointer. This pointer is passed to the <i>callback</i> function along with details of the event.

### -param eventsHandle [out]

Type: <b>HANDLE*</b>

Handle to the newly created subscription.

## -returns

Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The subscription was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>

## -remarks

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_SUBSCRIBE</a> access to the net event's container.

## -see-also

<a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback0">FWPM_NET_EVENT_CALLBACK0</a>



[FWPM_NET_EVENT_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventunsubscribe0">FwpmNetEventUnsubscribe0</a>

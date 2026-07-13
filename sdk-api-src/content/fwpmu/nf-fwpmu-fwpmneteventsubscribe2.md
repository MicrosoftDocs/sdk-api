---
UID: NF:fwpmu.FwpmNetEventSubscribe2
title: FwpmNetEventSubscribe2 function (fwpmu.h)
description: Is used to request the delivery of notifications regarding a particular net event. (FwpmNetEventSubscribe2)
helpviewer_keywords: ["FwpmNetEventSubscribe2","FwpmNetEventSubscribe2 function [Filtering]","fwp.fwpmneteventsubscribe2","fwpmu/FwpmNetEventSubscribe2"]
old-location: fwp\fwpmneteventsubscribe2.htm
tech.root: fwp
ms.assetid: CC55CA33-A153-4B48-AA89-A28F010024F7
ms.date: 12/05/2018
ms.keywords: FwpmNetEventSubscribe2, FwpmNetEventSubscribe2 function [Filtering], fwp.fwpmneteventsubscribe2, fwpmu/FwpmNetEventSubscribe2
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - FwpmNetEventSubscribe2
 - fwpmu/FwpmNetEventSubscribe2
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
 - FwpmNetEventSubscribe2
---

# FwpmNetEventSubscribe2 function


## -description

The <b>FwpmNetEventSubscribe2</b> function  is used to request the delivery of notifications regarding a particular net event.
<div class="alert"><b>Note</b>  <b>FwpmNetEventSubscribe2</b> is the specific implementation of <b>FwpmNetEventSubscribe</b> used in Windows 10, version 1607 and later. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8,  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1">FwpmNetEventSubscribe1</a> is available. For Windows 7, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe0">FwpmNetEventSubscribe0</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param subscription [in]

An [FWPM_NET_EVENT_SUBSCRIPTION0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0) structure which describes which notifications will be delivered. 

### -param callback [in]

Pointer to a function of type [FWPM_NET_EVENT_CALLBACK2](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_net_event_callback2) that will be invoked when a notification is ready for delivery.

### -param context [in, optional]

Optional context pointer. This pointer is passed to the <i>callback</i> function along with details of the event.

### -param eventsHandle [out]

Handle to the newly created subscription. Call [FwpmNetEventUnsubscribe0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmneteventunsubscribe0) to close this handle when the subscription is no longer needed.

## -returns

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

<a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback2">FWPM_NET_EVENT_CALLBACK2</a>



[FWPM_NET_EVENT_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventunsubscribe0">FwpmNetEventUnsubscribe0</a>

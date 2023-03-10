---
UID: NF:fwpmu.FwpmConnectionSubscribe0
title: FwpmConnectionSubscribe0 function (fwpmu.h)
description: Is used to request the delivery of notifications about changes to a connection object.
helpviewer_keywords: ["FwpmConnectionSubscribe0","FwpmConnectionSubscribe0 function [Filtering]","fwp.fwpmconnectionsubscribe0","fwpmu/FwpmConnectionSubscribe0"]
old-location: fwp\fwpmconnectionsubscribe0.htm
tech.root: fwp
ms.assetid: 86fe40b0-aada-44e1-91dd-0e825589159d
ms.date: 12/05/2018
ms.keywords: FwpmConnectionSubscribe0, FwpmConnectionSubscribe0 function [Filtering], fwp.fwpmconnectionsubscribe0, fwpmu/FwpmConnectionSubscribe0
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FwpmConnectionSubscribe0
 - fwpmu/FwpmConnectionSubscribe0
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
 - FwpmConnectionSubscribe0
---

## -description

The <b>FwpmConnectionSubscribe0</b> function is used to request the delivery of notifications about changes to a connection object.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param subscription [in]

Type: **[FWPM_CONNECTION_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)\***

The notifications which will be delivered.

### -param callback [in]

Type: <b><a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_connection_callback0">FWPM_CONNECTION_CALLBACK0</a></b>

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

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_SUBSCRIBE</a> access to the connection object's container.

## -see-also

<a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_connection_callback0">FWPM_CONNECTION_CALLBACK0</a>



[FWPM_CONNECTION_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0">FwpmConnectionUnsubscribe0</a>

---
UID: NF:fwpmu.IPsecSaContextSubscribe0
title: IPsecSaContextSubscribe0 function (fwpmu.h)
description: Is used to request the delivery of notifications regarding a particular IPsec security association (SA) context.
helpviewer_keywords: ["IPsecSaContextSubscribe0","IPsecSaContextSubscribe0 function [Filtering]","fwp.ipsecsacontextsubscribe0","fwpmu/IPsecSaContextSubscribe0"]
old-location: fwp\ipsecsacontextsubscribe0.htm
tech.root: fwp
ms.assetid: dadb22b2-6b20-401f-b2b5-256135a345b1
ms.date: 12/05/2018
ms.keywords: IPsecSaContextSubscribe0, IPsecSaContextSubscribe0 function [Filtering], fwp.ipsecsacontextsubscribe0, fwpmu/IPsecSaContextSubscribe0
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
 - IPsecSaContextSubscribe0
 - fwpmu/IPsecSaContextSubscribe0
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
 - IPsecSaContextSubscribe0
---

# IPsecSaContextSubscribe0 function


## -description

The <b>IPsecSaContextSubscribe0</b> function is used to request the delivery of notifications regarding a particular IPsec security association (SA) context.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param subscription [in]

Type: <b>const <a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0">IPSEC_SA_CONTEXT_SUBSCRIPTION0</a>*</b>

The notifications which will be delivered.

### -param callback [in]

Type: <b><a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0">IPSEC_SA_CONTEXT_CALLBACK0</a></b>

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

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_SUBSCRIBE</a> access to the IPsec SA context's container.

## -see-also

<a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0">IPSEC_SA_CONTEXT_CALLBACK0</a>



<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0">IPSEC_SA_CONTEXT_SUBSCRIPTION0</a>
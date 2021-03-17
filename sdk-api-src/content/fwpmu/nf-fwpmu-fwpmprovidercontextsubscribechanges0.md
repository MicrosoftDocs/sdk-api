---
UID: NF:fwpmu.FwpmProviderContextSubscribeChanges0
title: FwpmProviderContextSubscribeChanges0 function (fwpmu.h)
description: Is used to request the delivery of notifications regarding changes in a particular provider context.
helpviewer_keywords: ["FwpmProviderContextSubscribeChanges0","FwpmProviderContextSubscribeChanges0 function [Filtering]","fwp.fwpmprovidercontextsubscribechanges0_func","fwpmu/FwpmProviderContextSubscribeChanges0"]
old-location: fwp\fwpmprovidercontextsubscribechanges0_func.htm
tech.root: fwp
ms.assetid: cd8c9ec5-c93c-45e5-8a91-88bd89e465d7
ms.date: 12/05/2018
ms.keywords: FwpmProviderContextSubscribeChanges0, FwpmProviderContextSubscribeChanges0 function [Filtering], fwp.fwpmprovidercontextsubscribechanges0_func, fwpmu/FwpmProviderContextSubscribeChanges0
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FwpmProviderContextSubscribeChanges0
 - fwpmu/FwpmProviderContextSubscribeChanges0
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
 - FwpmProviderContextSubscribeChanges0
---

# FwpmProviderContextSubscribeChanges0 function


## -description

The <b>FwpmProviderContextSubscribeChanges0</b> function  is used to request the delivery of notifications regarding changes in a particular provider context.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param subscription [in]

Type: <b>const <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0">FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0</a>*</b>

The notifications to be delivered.

### -param callback [in]

Type: <b><a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_provider_context_change_callback0">FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0</a></b>

Function pointer that will be invoked when a notification is ready for delivery.

### -param context [in, optional]

Type: <b>void*</b>

Optional context pointer. This pointer is passed to the <i>callback</i> function along with details of the change.

### -param changeHandle [out]

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

Subscribers do not receive notifications for changes made with the same session handle used to subscribe. This is because subscribers only need  to see changes made by others since they already know which changes they made themselves.

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_SUBSCRIBE</a> access to the provider context's container and 
   <b>FWPM_ACTRL_READ</b> access to the provider context. The subscriber will only get notifications for provider contexts to which it has
   <b>FWPM_ACTRL_READ</b> access. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmProviderContextSubscribeChanges0</b> is a specific implementation of FwpmProviderContextSubscribeChanges. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_provider_context_change_callback0">FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0</a>



<a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0">FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0</a>
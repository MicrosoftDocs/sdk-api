---
UID: NF:fwpmu.FwpmProviderSubscribeChanges0
title: FwpmProviderSubscribeChanges0 function (fwpmu.h)
description: Is used to request the delivery of notifications regarding changes in a particular provider.helpviewer_keywords: ["FwpmProviderSubscribeChanges0","FwpmProviderSubscribeChanges0 function [Filtering]","fwp.fwpmprovidersubscribechanges0_func","fwpmu/FwpmProviderSubscribeChanges0"]
old-location: fwp\fwpmprovidersubscribechanges0_func.htm
tech.root: fwp
ms.assetid: 73d04bcb-b888-4e40-90e6-a0d777f926ef
ms.date: 12/05/2018
ms.keywords: FwpmProviderSubscribeChanges0, FwpmProviderSubscribeChanges0 function [Filtering], fwp.fwpmprovidersubscribechanges0_func, fwpmu/FwpmProviderSubscribeChanges0
f1_keywords:
- fwpmu/FwpmProviderSubscribeChanges0
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Fwpuclnt.dll
api_name:
- FwpmProviderSubscribeChanges0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmProviderSubscribeChanges0 function


## -description


The <b>FwpmProviderSubscribeChanges0</b> function  is used to request the delivery of notifications regarding changes in a particular provider.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param subscription [in, optional]

Type: [FWPM_PROVIDER_SUBSCRIPTION0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)a>*</b>

The notifications to be delivered.


### -param callback [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_provider_change_callback0">FWPM_PROVIDER_CHANGE_CALLBACK0</a></b>

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
A Windows Filtering Platform (WFP) specific error. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://docs.microsoft.com/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_SUBSCRIBE</a> access to the provider's container and 
   <b>FWPM_ACTRL_READ</b> access to the provider. The subscriber will only get notifications for providers to which it has
   <b>FWPM_ACTRL_READ</b> access. See <a href="https://docs.microsoft.com/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmProviderSubscribeChanges0</b> is a specific implementation of FwpmProviderSubscribeChanges. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_provider_change_callback0">FWPM_PROVIDER_CHANGE_CALLBACK0</a>



[FWPM_PROVIDER_SUBSCRIPTION0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)a>
 

 


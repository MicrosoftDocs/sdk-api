---
UID: NF:fwpmu.FwpmCalloutSubscriptionsGet0
title: FwpmCalloutSubscriptionsGet0 function (fwpmu.h)
description: Retrieves an array of all the current callout change notification subscriptions.
helpviewer_keywords: ["FwpmCalloutSubscriptionsGet0","FwpmCalloutSubscriptionsGet0 function [Filtering]","fwp.fwpmcalloutsubscriptionsget0_func","fwpmu/FwpmCalloutSubscriptionsGet0"]
old-location: fwp\fwpmcalloutsubscriptionsget0_func.htm
tech.root: fwp
ms.assetid: 72e51167-c69e-4412-b83e-c66f91c9b96e
ms.date: 12/05/2018
ms.keywords: FwpmCalloutSubscriptionsGet0, FwpmCalloutSubscriptionsGet0 function [Filtering], fwp.fwpmcalloutsubscriptionsget0_func, fwpmu/FwpmCalloutSubscriptionsGet0
f1_keywords:
- fwpmu/FwpmCalloutSubscriptionsGet0
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
- FwpmCalloutSubscriptionsGet0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmCalloutSubscriptionsGet0 function


## -description


The <b>FwpmCalloutSubscriptionsGet0</b> function retrieves an array of all the current callout change notification subscriptions.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param entries [out]

Type: [FWPM_CALLOUT_SUBSCRIPTION0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)***</b>

Addresses of the current callout change notification subscriptions.


### -param numEntries [out]

Type: <b>UINT32*</b>

The number of entries returned.


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
The subscriptions were retrieved successfully.

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



The returned array (but not the individual entries in the array) must be freed through a call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the callout's container. See <a href="https://docs.microsoft.com/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmCalloutSubscriptionsGet0</b> is a specific implementation of FwpmCalloutSubscriptionsGet. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




[FWPM_CALLOUT_SUBSCRIPTION0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)
 

 


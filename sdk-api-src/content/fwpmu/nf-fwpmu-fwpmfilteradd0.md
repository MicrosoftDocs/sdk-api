---
UID: NF:fwpmu.FwpmFilterAdd0
title: FwpmFilterAdd0 function (fwpmu.h)
description: Adds a new filter object to the system.
old-location: fwp\fwpmfilteradd0_func.htm
tech.root: fwp
ms.assetid: ca11187e-3a91-438f-9a7f-606da7c88f6d
ms.date: 12/05/2018
ms.keywords: FwpmFilterAdd0, FwpmFilterAdd0 function [Filtering], fwp.fwpmfilteradd0_func, fwpmu/FwpmFilterAdd0
f1_keywords:
- fwpmu/FwpmFilterAdd0
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
- FwpmFilterAdd0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmFilterAdd0 function


## -description


The <b>FwpmFilterAdd0</b> function adds a new filter object to the system.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param filter [in]

Type: [FWPM_FILTER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)a>*</b>

The filter object to be added.


### -param sd [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a></b>

Security information about the filter object.


### -param id [out, optional]

Type: <b>UINT64*</b>

The runtime identifier for this filter.


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
The filter was successfully added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SECURITY_DESCR</b></dt>
<dt>0x8007053a</dt>
</dl>
</td>
<td width="60%">
The security descriptor structure is invalid. Or, a filter condition contains a security descriptor in absolute format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_CALLOUT_NOTIFICATION_FAILED</b></dt>
<dt>0x80320037</dt>
</dl>
</td>
<td width="60%">
The caller added a callout
   filter and the callout returned an error from its notification routine.

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



<b>FwpmFilterAdd0</b> adds the filter to the specified sub-layer at every filtering layer in the system.

Some fields in the [FWPM_FILTER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)a> structure are assigned by the system, not the caller, and are ignored in the call to <b>FwpmFilterAdd0</b>. 

If the caller supplies a <b>NULL</b> security descriptor, the system will assign a default security descriptor.

To block connections to particular locations, add a  [FWP_ACTION_BLOCK](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_action0)a>filter specifying the local address at the <a href="https://docs.microsoft.com/windows/desktop/FWP/management-filtering-layer-identifiers-">FWPM_LAYER_ALE_AUTH_CONNECT_V*</a> 
layer, or add a  <b>FWP_ACTION_BLOCK</b>filter without specifying the local address at the <b>FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V*</b> layer.

[FWP_EMPTY](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_data_type)a>. </div>
<div> </div>
The [FWPM_FILTER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)a> structure can label a filter as a boot-time or persistent filter.  Boot-time filters are added to the Base Filtering Engine (BFE) when the TCP/IP driver starts, and are removed once the BFE finishes initialization.  Persistent objects are added when the BFE starts.

This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="https://docs.microsoft.com/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs the following access rights:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD</a> access to the filter's container</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD_LINK </a> access to the provider (if any)</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD_LINK </a> access to the applicable layer</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD_LINK </a> access to the applicable sub-layer</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD_LINK </a> access to the callout (if any)</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD_LINK </a> access to the provider context (if any).</li>
</ul>
  See <a href="https://docs.microsoft.com/windows/desktop/FWP/access-control">Access Control</a> for more information.

To add a filter that references a callout, invoke the functions in the following order.

<ul>
<li>Call <a href="https://go.microsoft.com/fwlink/p/?linkid=199850">FwpsCalloutRegister0</a> (documented in the Windows Driver Kit (WDK)), to register the callout with the filter engine.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutadd0">FwpmCalloutAdd0</a> to add the callout to the system.</li>
<li>Call <b>FwpmFilterAdd0</b> to add the filter that references the callout to the system.</li>
</ul>
By default filters that reference callouts that have been added but have not yet registered with the filter engine are treated as Block filters.

<b>FwpmFilterAdd0</b> is a specific implementation of FwpmFilterAdd. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example shows how to initialize and add a filter using <b>FwpmFilterAdd0</b> that 	   
specifically blocks traffic on IP V4 for all applications.


```cpp

// Add filter to block traffic on IP V4 for all applications. 
//
FWPM_FILTER0      fwpFilter;
FWPM_SUBLAYER0    fwpFilterSubLayer;  

RtlZeroMemory(&fwpFilter, sizeof(FWPM_FILTER0));

fwpFilter.layerKey = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4;
fwpFilter.action.type = FWP_ACTION_BLOCK;

if (&fwpFilterSubLayer.subLayerKey != NULL)
    fwpFilter.subLayerKey = fwpFilterSubLayer.subLayerKey;

fwpFilter.weight.type = FWP_EMPTY; // auto-weight.
fwpFilter.numFilterConditions = 0; // this applies to all application traffic
fwpFilter.displayData.name = L"Receive/Accept Layer Block";
fwpFilter.displayData.description = L"Filter to block all inbound connections.";
       
printf("Adding filter to block all inbound connections.\n");
result = FwpmFilterAdd0(engineHandle, &fwpFilter, NULL, NULL);
        
if (result != ERROR_SUCCESS)
    printf("FwpmFilterAdd0 failed. Return value: %d.\n", result);
else
    printf("Filter added successfully.\n");

```





## -see-also




[FWPM_FILTER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-mgmt-functions">Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-functions">WFP  Functions</a>
 

 


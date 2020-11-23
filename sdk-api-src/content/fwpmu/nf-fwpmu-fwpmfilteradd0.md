---
UID: NF:fwpmu.FwpmFilterAdd0
title: FwpmFilterAdd0 function (fwpmu.h)
description: Adds a new filter object to the system.
helpviewer_keywords: ["FwpmFilterAdd0","FwpmFilterAdd0 function [Filtering]","fwp.fwpmfilteradd0_func","fwpmu/FwpmFilterAdd0"]
old-location: fwp\fwpmfilteradd0_func.htm
tech.root: fwp
ms.assetid: ca11187e-3a91-438f-9a7f-606da7c88f6d
ms.date: 12/05/2018
ms.keywords: FwpmFilterAdd0, FwpmFilterAdd0 function [Filtering], fwp.fwpmfilteradd0_func, fwpmu/FwpmFilterAdd0
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
 - FwpmFilterAdd0
 - fwpmu/FwpmFilterAdd0
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
 - FwpmFilterAdd0
---

# FwpmFilterAdd0 function


## -description

The **FwpmFilterAdd0** function adds a new filter object to the system.

## -parameters

### -param engineHandle [in]

Type: **HANDLE**

Handle for an open session to the filter engine. Call  [FwpmEngineOpen0](nf-fwpmu-fwpmengineopen0.md) to open a session to the filter engine.

### -param filter [in]

Type: **[FWPM_FILTER0](../fwpmtypes/ns-fwpmtypes-fwpm_filter0.md)***

The filter object to be added.

### -param sd [in, optional]

Type: **[SECURITY_DESCRIPTOR](../winnt/ns-winnt-security_descriptor.md)**

Security information about the filter object.

### -param id [out, optional]

Type: **UINT64***

The runtime identifier for this filter.

## -returns

Type: **DWORD**

| Return code/value | Description |
| ----------------- | ----------- |
| ERROR_SUCCESS <br/> 0 | The filter was successfully added. |
| ERROR_INVALID_SECURITY_DESCR <br/> 0x8007053A | The security descriptor structure is invalid. Or, a filter condition contains a security descriptor in absolute format. |
| FWP_E_CALLOUT_NOTIFICATION_FAILED <br/> 0x80320037 | The caller added a callout filter and the callout returned an error from its notification routine. |
| FWP_E_* error code <br/> 0x80320001—0x80320039 | A Windows Filtering Platform (WFP) specific error. See [WFP Error Codes](/windows/desktop/FWP/wfp-error-codes) for details. |
| RPC_* error code <br/> 0x80010001—0x80010122 | Failure to communicate with the remote or local firewall engine. |

## -remarks

**FwpmFilterAdd0** adds the filter to the specified sub-layer at every filtering layer in the system.

Some fields in the [FWPM_FILTER0](../fwpmtypes/ns-fwpmtypes-fwpm_filter0.md) structure are assigned by the system, not the caller, and are ignored in the call to **FwpmFilterAdd0**.

If the caller supplies a **NULL** security descriptor, the system will assign a default security descriptor.

To block connections to particular locations, add a [FWP_ACTION_BLOCK](../fwpmtypes/ns-fwpmtypes-fwpm_action0.md) filter specifying the local address at the [FWPM_LAYER_ALE_AUTH_CONNECT_V*](/windows/desktop/FWP/management-filtering-layer-identifiers-) layer, or add a **FWP_ACTION_BLOCK** filter without specifying the local address at the **FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V*** layer.

> [!Note]
> If a local address is specified at the resource assignment layer, an implicit bind would succeed because address, address type, and port may come back as [FWP_EMPTY](../fwptypes/ne-fwptypes-fwp_data_type.md).

The [FWPM_FILTER0](../fwpmtypes/ns-fwpmtypes-fwpm_filter0.md) structure can label a filter as a boot-time or persistent filter.  Boot-time filters are added to the Base Filtering Engine (BFE) when the TCP/IP driver starts, and are removed once the BFE finishes initialization.  Persistent objects are added when the BFE starts.

This function cannot be called from within a read-only transaction. It will fail with **FWP_E_INCOMPATIBLE_TXN**. See [Object Management](/windows/desktop/FWP/object-management) for more information about transactions.

The caller needs the following access rights:

- [FWPM_ACTRL_ADD](/windows/desktop/FWP/access-right-identifiers) access to the filter's container
- [FWPM_ACTRL_ADD_LINK](/windows/desktop/FWP/access-right-identifiers) access to the provider (if any)
- [FWPM_ACTRL_ADD_LINK](/windows/desktop/FWP/access-right-identifiers) access to the applicable layer
- [FWPM_ACTRL_ADD_LINK](/windows/desktop/FWP/access-right-identifiers) access to the applicable sub-layer
- [FWPM_ACTRL_ADD_LINK](/windows/desktop/FWP/access-right-identifiers) access to the callout (if any)
- [FWPM_ACTRL_ADD_LINK](/windows/desktop/FWP/access-right-identifiers) access to the provider context (if any).
  
See [Access Control](/windows/desktop/FWP/access-control) for more information.

To add a filter that references a callout, invoke the functions in the following order.

- Call [FwpsCalloutRegister0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscalloutregister0) (documented in the Windows Driver Kit (WDK)), to register the callout with the filter engine.
- Call [FwpmCalloutAdd0](nf-fwpmu-fwpmcalloutadd0.md) to add the callout to the system.
- Call **FwpmFilterAdd0** to add the filter that references the callout to the system.

By default filters that reference callouts that have been added but have not yet registered with the filter engine are treated as Block filters.

**FwpmFilterAdd0** is a specific implementation of FwpmFilterAdd. See [WFP Version-Independent Names and Targeting Specific Versions of Windows](/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows)  for more information.

#### Examples

The following C++ example shows how to initialize and add a filter using **FwpmFilterAdd0** that 	   
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

[FWPM_FILTER0](../fwpmtypes/ns-fwpmtypes-fwpm_filter0.md)

[Management Functions](/windows/desktop/FWP/fwp-mgmt-functions)

[WFP  Functions](/windows/desktop/FWP/fwp-functions)

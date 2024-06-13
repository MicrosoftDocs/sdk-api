---
UID: NS:fwpstypes.FWPS_FILTER2_
title: FWPS_FILTER2 (fwpstypes.h)
description: The FWPS_FILTER2 structure defines a run-time filter in the filter engine.Note  FWPS_FILTER2 is the specific version of FWPS_FILTER used in Windows 8 and later.
helpviewer_keywords: ["FWPS_FILTER2","FWPS_FILTER2 structure [Network Drivers Starting with Windows Vista]","FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT","FWPS_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED","fwpstypes/FWPS_FILTER2","netvista.fwps_filter2"]
old-location: netvista\fwps_filter2.htm
tech.root: NetVista
ms.assetid: 2be2c82b-5b7c-4027-b2a1-f43d2b27b860
ms.date: 05/03/2024
ms.keywords: FWPS_FILTER2, FWPS_FILTER2 structure [Network Drivers Starting with Windows Vista], FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT, FWPS_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED, fwpstypes/FWPS_FILTER2, netvista.fwps_filter2
req.header: fwpstypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 8.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPS_FILTER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_FILTER2_
 - fwpstypes/FWPS_FILTER2_
 - FWPS_FILTER2
 - fwpstypes/FWPS_FILTER2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpstypes.h
api_name:
 - FWPS_FILTER2
---

## -description

Defines a run-time filter in the filter engine. The [FWPS_FILTER0](ns-fwpstypes-fwps_filter0.md) is available.

## -struct-fields

### -field filterId

A run-time identifier that identifies the filter in the filter engine.

### -field weight

An [FWP_VALUE0](../fwptypes/ns-fwptypes-fwp_value0.md) structure that contains a value that specifies the filter's importance in relation to other filters in the filter engine. Filters with a higher **weight** value are invoked first. The data type specified in the **FWP_VALUE0** structure is either **FWP_UINT64** or FWP_EMPTY. If the data type specified in the **FWP_VALUE0** structure is FWP_EMPTY, the filter engine automatically assigns a weight to the filter based on how specific the filter tests the data compared to the other filters in the filter engine.

### -field subLayerWeight

A value that specifies the importance of the filter's sublayer in relation to the other sublayers in the filter engine. Filters that are located in a sublayer with a higher **subLayerWeight** value are invoked first.

### -field flags

Flags that specify actions that a callout's [classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2) callout function should take when processing network data. Possible flags are:

| Value | Meaning |
| - | - |
| FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT | This flag indicates to a callout's [classifyFn0](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0) callout function that it should always clear the FWPS_RIGHT_ACTION_WRITE flag when it returns either FWP_ACTION_BLOCK or FWP_ACTION_PERMIT for the suggested action. If this flag is not set, a callout's ***classifyFn0*** callout function should only clear the FWPS_RIGHT_ACTION_WRITE flag when it returns FWP_ACTION_BLOCK for the suggested action. |
| FWPS_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED | This flag indicates to a callout's [classifyFn0](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0) callout function that if the callout is not registered, the callout should be treated as a permit filter. |

### -field numFilterConditions

The number of [FWPS_FILTER_CONDITION0](ns-fwpstypes-fwps_filter_condition0.md) structures in the array pointed to by the **filterCondition** member. This member can be zero.

### -field filterCondition

A pointer to an array of [FWPS_FILTER_CONDITION0](ns-fwpstypes-fwps_filter_condition0.md) structures. These structures define the run-time filtering conditions for the filter. If the **numFilterConditions** member is zero, then this pointer will be **NULL**.

### -field action

An [FWPS_ACTION0](ns-fwpstypes-fwps_action0.md) structure that specifies the action that the filter should take if all of the filter's filtering conditions are true.

### -field context

A context value that is associated with the filter. A callout can set this member to point to a callout driver-supplied context structure from within the callout driver's [notifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_notify_fn2) callout function when the filter is added to the filter engine. This context structure, which is opaque to the filter engine, can be used by the callout driver's [classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2) callout function to preserve any driver-specific data or state information between calls by the filter engine to the callout driver's ***classifyFn2*** callout function.

### -field providerContext

A pointer to the provider context, which is formatted as a [FWPM_PROVIDER_CONTEXT2](../fwpmtypes/ns-fwpmtypes-fwpm_provider_context2.md) structure. If the filter uses a callout, and the callout has the FWPM_CALLOUT_FLAG_USES_PROVIDER_CONTEXT flag set, this member will contain the provider context from the corresponding [FWPM_FILTER0](../fwpmtypes/ns-fwpmtypes-fwpm_filter0.md) structure. Otherwise, this parameter is **NULL**.

## -remarks

The filter engine passes a pointer to an **FWPS_FILTER2** structure to a callout's [notifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_notify_fn2) and [classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2) callout functions.

A filter's action is performed only if all of the filter's filtering conditions are true. If no filtering conditions are specified in the filter, then the specified action is always performed.

The **providerContext** member provides a mechanism for a callout driver to retrieve provider contexts without calling the base filtering engine (BFE).

This structure is essentially identical to the previous version, [FWPM_PROVIDER_CONTEXT2](../fwpmtypes/ns-fwpmtypes-fwpm_provider_context2.md) structure at the **providerContext** member.

## -see-also

[FWPM_FILTER0](../fwpmtypes/ns-fwpmtypes-fwpm_filter0.md)



[FWPM_PROVIDER_CONTEXT2](../fwpmtypes/ns-fwpmtypes-fwpm_provider_context2.md)



[FWPS_ACTION0](ns-fwpstypes-fwps_action0.md)



[FWPS_FILTER0](ns-fwpstypes-fwps_filter0.md)



[FWPS_FILTER1](ns-fwpstypes-fwps_filter1.md)



[FWPS_FILTER_CONDITION0](ns-fwpstypes-fwps_filter_condition0.md)



[FWP_VALUE0](../fwptypes/ns-fwptypes-fwp_value0.md)



[classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2)



[notifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_notify_fn2)

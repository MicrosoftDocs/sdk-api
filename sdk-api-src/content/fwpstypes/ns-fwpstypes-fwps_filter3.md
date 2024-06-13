---
UID: NS:fwpstypes.FWPS_FILTER3_
title: FWPS_FILTER3
description: Defines a run-time filter in the filter engine.
tech.root: NetVista
ms.date: 05/03/2024
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: fwpstypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: FWPS_FILTER3
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpstypes.h
api_name:
 - FWPS_FILTER3_
 - FWPS_FILTER3
f1_keywords:
 - FWPS_FILTER3_
 - fwpstypes/FWPS_FILTER3_
 - FWPS_FILTER3
 - fwpstypes/FWPS_FILTER3
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FILTER3_
---

## -description

Defines a run-time filter in the filter engine. [FWPS_FILTER0](./ns-fwpstypes-fwps_filter0.md), [FWPS_FILTER1](./ns-fwpstypes-fwps_filter1.md), and [FWPS_FILTER2](./ns-fwpstypes-fwps_filter2.md) are available.

## -struct-fields

### -field filterId

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

A run-time identifier that identifies the filter in the filter engine.

### -field weight

Type: **[FWP_VALUE0](/windows/win32/api/fwptypes/ns-fwptypes-fwp_value0)**

A value that specifies the filter's importance in relation to other filters in the filter engine. Filters with a higher weight value are invoked first. The data type specified in the **FWP_VALUE0** structure is either **FWP_UINT64** or **FWP_EMPTY**. If the data type specified in the **FWP_VALUE0** structure is **FWP_EMPTY**, then the filter engine automatically assigns a weight to the filter based on how specific the filter tests the data compared to the other filters in the filter engine.

### -field subLayerWeight

Type: **[UINT16](/windows/win32/winprog/windows-data-types)**

A value that specifies the importance of the filter's sublayer in relation to the other sublayers in the filter engine. Filters that are located in a sublayer with a higher *subLayerWeight* value are invoked first.

### -field flags

Type: **[UINT16](/windows/win32/winprog/windows-data-types)**

Flags that specify actions that a callout's [classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2) callout function should take when processing network data. Possible flags are:

| Value | Meaning |
| - | - |
| FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT | This flag indicates to a callout's [classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2) callout function that it should always clear the FWPS_RIGHT_ACTION_WRITE flag when it returns either FWP_ACTION_BLOCK or FWP_ACTION_PERMIT for the suggested action. |
| FWPS_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED | This flag indicates to a callout's [classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2) callout function that if the callout is not registered, then the callout should be treated as a permit filter. |

### -field numFilterConditions

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of [FWPS_FILTER_CONDITION0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_filter_condition0) structures in the array pointed to by *filterCondition*. The number can be zero.

### -field filterCondition

Type: **[FWPS_FILTER_CONDITION0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_filter_condition0)\***

A pointer to an array of [FWPS_FILTER_CONDITION0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_filter_condition0) structures. These structures define the run-time filtering conditions for the filter. If *numFilterConditions* is zero, then this pointer will be NULL.

### -field action

Type: **[FWPS_ACTION0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_action0)**

Specifies the action that the filter should take if all of the filter's filtering conditions are true.

### -field context

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

A context value that's associated with the filter. A callout can set this member to point to a callout driver-supplied context structure from within the callout driver's [classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2) callout function when the filter is added to the filter engine. This context structure, which is opaque to the filter engine, can be used by the callout driver's [classifyFn2](/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn2) callout function to preserve any driver-specific data or state information between calls by the filter engine to the callout driver's **classifyFn2** callout function.

### -field providerContext

Type: **[FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3)\***

A pointer to the provider context, which is formatted as a [FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3) structure. If the filter uses a callout, and the callout has the **FWPM_CALLOUT_FLAG_USES_PROVIDER_CONTEXT** flag set, then this member will contain the provider context from the corresponding [FWPM_FILTER0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0) structure. Otherwise, this member is NULL.

## -remarks

The filter engine passes a pointer to an **FWPS_FILTER3** structure to a callout's **notifyFn3** and **classifyFn3** callout functions.

A filter's action is performed only if all of the filter's filtering conditions are true. If no filtering conditions are specified in the filter, then the specified action is always performed.

The *providerContext* member provides a mechanism for a callout driver to retrieve provider contexts without calling the base filtering engine (BFE).

This structure is essentially identical to the previous version, [FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3) structure at the *providerContext* member.

## -see-also

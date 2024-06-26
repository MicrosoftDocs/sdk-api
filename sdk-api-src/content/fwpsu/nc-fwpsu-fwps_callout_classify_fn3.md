---
UID: NC:fwpsu.FWPS_CALLOUT_CLASSIFY_FN3
tech.root: fwp
title: FWPS_CALLOUT_CLASSIFY_FN3
ms.date: 06/07/2024
targetos: Windows
description: TBD
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fwpsu.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - fwpsu.h
api_name:
 - FWPS_CALLOUT_CLASSIFY_FN3
f1_keywords:
 - FWPS_CALLOUT_CLASSIFY_FN3
 - fwpsu/FWPS_CALLOUT_CLASSIFY_FN3
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_CALLOUT_CLASSIFY_FN3
---

## -description

Version 3 of the callback function invoked during classification when a callout filter matches. The difference being that this callback returns an [FWPS_FILTER3](../fwpstypes/ns-fwpstypes-fwps_filter3.md) structure.

## -parameters

### -param inFixedValues

A pointer to an [FWPS_INCOMING_VALUES0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_incoming_values0) structure. This structure contains the values for each of the data fields at the layer being filtered.

### -param inMetaValues

A pointer to an [FWPS_INCOMING_METADATA_VALUES0](/windows/win32/api/fwpsu/ns-fwpsu-fwps_incoming_metadata_values0) structure. This structure contains the values for each of the metadata fields at the layer being filtered.

### -param layerData

A pointer to a structure that describes the raw data at the layer being filtered. This parameter might be **NULL**, depending on the layer being filtered and the conditions under which the **classifyFn3** callout function is called. For the stream layer, this parameter points to an **FWPS_STREAM_CALLOUT_IO_PACKET0** structure. For all of the other layers, this parameter points to a **NET_BUFFER_LIST** structure if it is not **NULL**.

### -param classifyContext

A pointer to context data associated with the callout driver by the filter engine.

### -param filter

A pointer to an [FWPS_FILTER3](../fwpstypes/ns-fwpstypes-fwps_filter3.md) structure. This structure describes the filter that specifies the callout for the filter's action.

### -param flowContext

A UINT64-typed variable that contains the context associated with the data flow. If no context is associated with the data flow, then this parameter is zero. If the callout is added to the filter engine at a filtering layer that does not support data flows, the **classifyFn3** callout function should ignore this parameter.

### -param classifyOut

A pointer to an [FWPS_CLASSIFY_OUT0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) structure that receives any data that the **classifyFn3** callout function returns to the caller.

## -remarks

A callout driver registers a callout's callout functions with the filter engine by calling the **FwpsCalloutRegister2** function.

The filter engine calls a callout's **classifyFn3** callout function with data to be processed whenever all of the test conditions are true for a filter in the filter engine that specifies the callout for the filter's action.

A callout's **classifyFn1** callout function should clear the **FWPS_RIGHT_ACTION_WRITE** flag in the *rights* member of the [FWPS_CLASSIFY_OUT0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) structure in any of the following situations:

* When the **classifyFn1** callout function sets the *actionType* member of the **FWPS_CLASSIFY_OUT0** structure to **FWP_ACTION_BLOCK**.
* When the **classifyFn1** callout function sets the *actionType* member of the **FWPS_CLASSIFY_OUT0** structure to **FWP_ACTION_PERMIT** and the **FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT** flag is set in the *flags* member of the [FWPS_FILTER3](../fwpstypes/ns-fwpstypes-fwps_filter3.md) structure.
* When a callout has indicated that it intends to modify the clone net buffer list by setting the *intendToModify* parameter to **TRUE** in a call to the **FwpsReferenceNetBufferList0** function.

## -see-also

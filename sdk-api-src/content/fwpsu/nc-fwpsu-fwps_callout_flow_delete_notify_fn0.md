---
UID: NC:fwpsu.FWPS_CALLOUT_FLOW_DELETE_NOTIFY_FN0
tech.root: fwp
title: FWPS_CALLOUT_FLOW_DELETE_NOTIFY_FN0
ms.date: 06/07/2024
targetos: Windows
description: The filter engine calls a callout's flowDeleteFn callout function to notify the callout that a data flow that is being processed by the callout is being terminated.
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
 - FWPS_CALLOUT_FLOW_DELETE_NOTIFY_FN0
f1_keywords:
 - FWPS_CALLOUT_FLOW_DELETE_NOTIFY_FN0
 - fwpsu/FWPS_CALLOUT_FLOW_DELETE_NOTIFY_FN0
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_CALLOUT_FLOW_DELETE_NOTIFY_FN0
---

## -description

The filter engine calls a callout's **flowDeleteFn** callout function to notify the callout that a data flow that is being processed by the callout is being terminated.

## -parameters

### -param layerId

The run-time identifier for the filtering layer at which the data flow is being terminated. For more information, see [Filtering layer identifiers](/windows/win32/fwp/management-filtering-layer-identifiers-).

### -param calloutId

The run-time identifier for the callout in the filter engine. This is the same identifier that was returned when the callout driver called either the **FwpsCalloutRegister0** or **FwpsCalloutRegister1** functions to register the callout with the filter engine.

### -param flowContext

The most recent context that has been associated with the data flow by a call to the **FwpsFlowAssociateContext0** function.

## -remarks

A callout driver registers a callout's callout functions with the filter engine by calling either the **FwpsCalloutRegister0** or **FwpsCalloutRegister1** functions.

The filter engine calls a callout's flowDeleteFn callout function when it terminates a data flow so that the callout can clean up the context associated with the data flow. For example, this callout function will be called after an abrupt halt from RST, without **classifyFn** being called first. The filter engine calls this callout function only if the callout driver associated a context with the data flow. The context will be automatically removed from the data flow by the filter engine when the data flow terminates.

The filter engine calls a callout's *flowDeleteFn* callout function only if the callout has been previously added to the filter engine at a filtering layer that supports data flows and the callout driver associates a context with the data flows that it processes. If a callout driver does not associate a context with the data flows that the callout processes, it should not implement a *flowDeleteFn* callout function for the callout. In this situation, the callout driver should set the *flowDeleteFn* member of the **FWPS_CALLOUT0** structure to **NULL** when it registers the callout with the filter engine.

The **FWPS_CALLOUT_FLOW_DELETE_NOTIFY_FN0** type is defined as a pointer to the *flowDeleteFn* function as follows.

```cpp
typedef void (NTAPI *FWPS_CALLOUT_FLOW_DELETE_NOTIFY_FN0) flowDeleteFn
```

The filter engine calls a callout's *flowDeleteFn* callout function at IRQL <= DISPATCH_LEVEL.

## -see-also

---
UID: NC:fwpsu.FWPS_CALLOUT_NOTIFY_FN0
tech.root: fwp
title: FWPS_CALLOUT_NOTIFY_FN0
ms.date: 06/07/2024
targetos: Windows
description: The filter engine calls a callout's notifyFn0 callout function to notify the callout driver about events that are associated with the callout.
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
 - FWPS_CALLOUT_NOTIFY_FN0
f1_keywords:
 - FWPS_CALLOUT_NOTIFY_FN0
 - fwpsu/FWPS_CALLOUT_NOTIFY_FN0
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_CALLOUT_NOTIFY_FN0
---

## -description

The filter engine calls a callout's **notifyFn0** callout function to notify the callout driver about events that are associated with the callout.

> [!NOTE]
> **notifyFn0** is the specific version of **notifyFn** used in Windows Vista and later. For more info, see [WFP version-independent names and targeting specific versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows). For Windows 8, **notifyFn2** is available. For Windows 7, **notifyFn1** is available.

## -parameters

### -param notifyType

A value that indicates the type of notification that the filter engine is sending to the callout. Valid values for this parameter are:

**FWPS_CALLOUT_NOTIFY_ADD_FILTER**. A filter is being added to the filter engine that specifies the callout for the filter's action.

**FWPS_CALLOUT_NOTIFY_DELETE_FILTER**. A filter is being deleted from the filter engine that specifies the callout for the filter's action.

**FWPS_CALLOUT_NOTIFY_TYPE_MAX**. A maximum value for testing purposes.

### -param filterKey

A pointer to the management identifier for the filter, as specified by the application or driver that is adding or deleting the filter. Must be **NULL** if the *notifyType* parameter is set to **FWPS_CALLOUT_NOTIFY_DELETE_FILTER**. For more information, see Remarks.

### -param filter

A pointer to an [FWPS_FILTER0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_filter0) structure. This structure describes the filter that is being added to or deleted from the filter engine.

A callout's **notifyFn0** callout function can set the *context* member of this structure to point to a callout driver-supplied context structure when the filter is added to the filter engine. This context structure is opaque to the filter engine, and can be used by the callout driver's **classifyFn0** callout function to preserve any driver-specific data or state information between calls by the filter engine to the callout driver's
**classifyFn0** callout function.

A callout's **notifyFn0** callout function can clean up any context associated with the filter when the filter is deleted from the filter engine.

## -returns

A callout's **notifyFn0** function returns one of the following **NTSTATUS** codes.

|Return code|Description|
|-|-|
|STATUS_SUCCESS|The callout driver accepts the notification from the filter engine.|
|Other status codes|An error occurred. If the *notifyType* parameter is **FWPS_CALLOUT_NOTIFY_ADD_FILTER**, the filter will not be added to the filter engine. If the *notifyType* parameter is **FWPS_CALLOUT_NOTIFY_DELETE_FILTER**, the filter will still be deleted from the filter engine.|

## -remarks

A callout driver registers a callout's callout functions with the filter engine by calling the **FwpsCalloutRegister0** function.

The filter engine calls a callout's **notifyFn0** callout function to notify the callout driver about events that are associated with the callout. If the callout driver's **notifyFn0** callout function does not recognize the type of notification that is passed in the *notifyType* parameter, it ignores the notification and return **STATUS_SUCCESS**.

If a callout driver registers a callout with the filter engine after filters that specify the callout for the filter's action have already been added to the filter engine, the filter engine does not call the callout driver's **notifyFn0** callout function to notify the callout about any of the existing filters. The filter engine calls the callout driver's **notifyFn0** callout function to notify the callout when new filters that specify the callout for the filter's action are added to the filter engine. In this situation, a callout's **notifyFn0** callout function might not get called for every filter in the filter engine that specifies the callout for the filter's action. If a callout driver registers a callout after the filter engine is started and the callout needs to know about every filter in the filter engine that specifies the callout for the filter's action, the callout driver must call the appropriate management functions to enumerate all the filters in the filter engine and sort through the resulting list of filters to find those that specify the callout for the filter's action. See [Calling other Windows Filtering Platform functions](/windows-hardware/drivers/network/calling-other-windows-filtering-platform-functions) for more information about calling these functions.

When a filter that specifies a callout for the filter's action is deleted from the filter engine, the filter engine calls the callout driver's **notifyFn0** callout function and passes FWP_CALLOUT_NOTIFY_DELETE_FILTER in the notifyType parameter and **NULL** in the filterKey parameter. For more information, see [Processing notify callouts](/windows-hardware/drivers/network/processing-notify-callouts).

## -see-also

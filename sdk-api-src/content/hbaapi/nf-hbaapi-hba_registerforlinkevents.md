---
UID: NF:hbaapi.HBA_RegisterForLinkEvents
tech.root: hba
title: HBA_RegisterForLinkEvents
ms.date: 08/02/2022
targetos: Windows
description: 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: hbaapi.h
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
 - HeaderDef
api_location:
 - hbaapi.h
api_name:
 - HBA_RegisterForLinkEvents
f1_keywords:
 - HBA_RegisterForLinkEvents
 - hbaapi/HBA_RegisterForLinkEvents
dev_langs:
 - c++
helpviewer_keywords:
 - HBA_RegisterForLinkEvents
---

## -description

Registers with a specified adapter for asynchronous fabric link-level events.

## -parameters

### -param callback

Pointer to a callback routine to be called when the event occurs. Define your callback routine with this prototype:

`void(*)(void *data, HBA_WWN adapterWWN, HBA_UINT32 eventType, void *pRLIRBuffer, HBA_UINT32 RLIRBufferSize)`

When your callback routine is called, the following parameters are passed to it:

* *data*. Pointer to a buffer that contains data that you provided when registering this callback routine. You can use this data to correlate the event with the source of the event registration.
* *adapterWWN*. A 64-bit world-wide name (WWN) that uniquely identifies the host bus adapter (HBA) from which the adapter event is being reported. The callback routine is called whenever an adapter event occurs for this HBA. For a discussion of worldwide names, see the T11 committee's *Fibre Channel HBA API* specification.
* *eventType*. Indicates the event type. The values assigned to this member correspond to the values associated with the [EVENT_TYPE_QUALIFIERS](/windows-hardware/drivers/storage/event-types-qualifiers) property qualifier. In particular, this member can have one of the following values: HBA_EVENT_LINK_UNKNOWN (a fabric link or topology change was detected by means other than a registered link incident report, or RLIR), or HBA_EVENT_LINK_INCIDENT (an RLIR has arrived).
* *pRLIRBuffer*. A buffer that contains the payload data of the RLIR associated with the event. If the RLIR payload exceeds the size of the buffer, then the data is truncated to the size of the buffer. The reported data is in big-endian format (that is, higher order bytes are in lower addresses).
* *RLIRBufferSize*. Indicates the size of the buffer at *pRLIRBuffer*.

### -param userData

Pointer to a buffer that will be passed to the callback routine with each event. This data correlates the event with the source of the event registration.

### -param pRLIRBuffer

Pointer to registered link incident report (RLIR) data that is passed to the callback routine with each occurrence of the event. This data is overwritten by the callback routine each time it is called.

### -param RLIRBufferSize

Contains the size, in bytes, of the buffer at *pRLIRBuffer*.

### -param Handle

Contains a value (returned by the routine [HBA_OpenAdapter](nf-hbaapi-hba_openadapter.md)) that identifies the HBA for which event callbacks are requested.

### -param pCallbackHandle

Contains an opaque identifier that you can pass to [HBA_RemoveCallback](nf-hbaapi-hba_removecallback.md) to de-register the callback routine.

## -returns

A value of type [HBA_STATUS](/windows-hardware/drivers/storage/hba-status) that indicates the status of the HBA. In particular, it returns one of the following values.

|Return code|Description|
|-|-|
|HBA_STATUS_OK|The callback routine was successfully registered.|
|HBA_STATUS_ERROR_NOT_SUPPORTED|Either the library or the system doesn't support events|
|HBA_STATUS_ERROR|An unspecified error occurred that prevented the registration of the callback routine.|

## -remarks

Only RLIR events are reported. To stop event delivery, call [HBA_RemoveCallback](nf-hbaapi-hba_removecallback.md).

## -see-also

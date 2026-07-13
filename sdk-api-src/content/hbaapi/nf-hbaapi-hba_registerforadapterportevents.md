---
UID: NF:hbaapi.HBA_RegisterForAdapterPortEvents
tech.root: hba
title: HBA_RegisterForAdapterPortEvents
ms.date: 08/02/2022
targetos: Windows
description: Registers the indicated user callback routine to call when a port event occurs.
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
 - HBA_RegisterForAdapterPortEvents
f1_keywords:
 - HBA_RegisterForAdapterPortEvents
 - hbaapi/HBA_RegisterForAdapterPortEvents
dev_langs:
 - c++
helpviewer_keywords:
 - HBA_RegisterForAdapterPortEvents
---

## -description

Registers the indicated user callback routine to call when a port event occurs.

## -parameters

### -param callback

Pointer to a callback routine to be called when the event occurs. Define your callback routine with this prototype:

`void(*)(void *pData, HBA_WWN PortWWN, HBA_UINT32 eventType, HBA_UINT32 fabricPortID)`

When your callback routine is called, the following parameters are passed to it:

* *pData*. Pointer to a buffer that contains data that you provided when registering this callback routine. You can use this data to correlate the event with the source of the event registration.
* *PortWWN*. A 64-bit world-wide name (WWN) that uniquely identifies the host bus adapter (HBA) port from which port events are reported. The callback routine is called whenever an event occurs for this port. For a discussion of worldwide names, see the T11 committee's *Fibre Channel HBA API* specification.
* *eventType*. Indicates the event type. The values assigned to this member correspond to the values associated with the [EVENT_TYPE_QUALIFIERS](/windows-hardware/drivers/storage/event-types-qualifiers) property qualifier. In particular, this member can have one of the following values: HBA_EVENT_PORT_FABRIC (a local port has received a registered state change notification, or RSCN, command. When this event occurs, *fabricPortID* contains the port identifier page for the sub-section of the fabric that has changed, as explained in the T11 committee's *Fibre Channel Framing and Signaling*, or FC-FS, specification), or HBA_EVENT_PORT_OFFLINE (a local port has gone offline), or HBA_EVENT_PORT_NEW_TARGETS (a local port has added target devices to its discovered remote ports), or HBA_EVENT_PORT_ONLINE (a local port has come online), or HBA_EVENT_PORT_UNKNOWN (the port event is unknown).
* *fabricPortID*. Pointer to a buffer that contains the port ID page for the sub-section of the fabric that has changed, as explained in the T11 committee's *Fibre Channel Framing and Signaling (FC-FS)* specification.

### -param UserData

Pointer to a buffer that will be passed to the callback routine with each event. This data correlates the event with the source of the event registration.

### -param Handle

Contains a value (returned by the routine [HBA_OpenAdapter](nf-hbaapi-hba_openadapter.md)) that identifies the HBA for which event callbacks are requested.

### -param PortWWN

A 64-bit world-wide name (WWN) that uniquely identifies the host bus adapter (HBA) port from which port events are reported. For a discussion of worldwide names, see the T11 committee's *Fibre Channel HBA API* specification.

### -param pCallbackHandle

Contains an opaque identifier that you can pass to [HBA_RemoveCallback](nf-hbaapi-hba_removecallback.md) to de-register the callback routine.

## -returns

A value of type [HBA_STATUS](/windows-hardware/drivers/storage/hba-status) that indicates the status of the HBA. In particular, it returns one of the following values.

|Return code|Description|
|-|-|
|HBA_STATUS_OK|The callback routine was successfully registered.|
|HBA_STATUS_ERROR_ILLEGAL_WWN|Returned if the HBA referenced by *handle* doesn't have a port with a name that matches the value in *PortWWN*.|
|HBA_STATUS_ERROR|An unspecified error occurred that prevented the registration of the callback routine.|

## -remarks

For a list of port events, see *eventType* in the *callback* parameter.

## -see-also

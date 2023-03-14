---
UID: NE:nvme.NVME_ASYNC_EVENT_NOTICE_CODES
tech.root: fs
title: NVME_ASYNC_EVENT_NOTICE_CODES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate a Notice event type.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_ASYNC_EVENT_NOTICE_CODES
f1_keywords:
 - NVME_ASYNC_EVENT_NOTICE_CODES
 - nvme/NVME_ASYNC_EVENT_NOTICE_CODES
dev_langs:
 - c++
---

# NVME_ASYNC_EVENT_NOTICE_CODES enumeration


## -description

Contains values that indicate a Notice event type.

## -enum-fields

### -field NVME_ASYNC_NOTICE_NAMESPACE_ATTRIBUTE_CHANGED

The [Identify Namespace data structure](../nvme/ns-nvme-nvme_identify_namespace_data.md) for one or more namespaces has changed.

Host software may use this event as an indication that it should read the [Identify Namespace](../nvme/ns-nvme-nvme_identify_namespace_data.md) data structures for each namespace to determine what has changed.

A controller should not send this event when [Namespace Utilization (NUSE)](../nvme/ns-nvme-nvme_identify_namespace_data.md) has changed, as this is a frequent event that does not require action by the host. A controller should only send this event for changes to the [Format Progress Indicator (FPI)](../nvme/ns-nvme-nvme_identify_namespace_data.md) field when bits `6:0` of that field transition from a non-zero value to zero or from a zero value to a non-zero value.

### -field NVME_ASYNC_NOTICE_FIRMWARE_ACTIVATION_STARTING

The controller is starting a firmware activation process during which command processing is paused.

Host software may use the Processing Paused (PP) field of [NVME_CONTROLLER_STATUS](ns-nvme-nvme_controller_status.md) to determine when command processing has resumed. To clear this event, the host software reads the [Firmware Slot Information log page](ns-nvme-nvme_firmware_slot_info_log.md).

### -field NVME_ASYNC_NOTICE_TELEMETRY_LOG_CHANGED

The controller has saved the controller internal state in the Telemetry Controller-Initiated log page and set the Telemetry Controller-Initiated Data Available field to 1h in that log page. To clear this event, the host issues a Get Log Page command with Retain Asynchronous Event bit cleared to ‘0’ for the Telemetry Controller-Initiated log.

## -remarks

Use this enumeration to specify values in the **NVME_ASYNC_EVENT_TYPE_NOTICE** field of the [NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md) enumeration that is used in the Async Event Request Admin command.

## -see-also

[NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md)
[NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md)
[NVME_FIRMWARE_SLOT_INFO_LOG](ns-nvme-nvme_firmware_slot_info_log.md)
[NVME_ADMIN_COMMANDS](ne-nvme-nvme_admin_commands.md)


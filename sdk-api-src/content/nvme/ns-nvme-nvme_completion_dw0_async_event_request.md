---
UID: NS:nvme.NVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
tech.root: fs
title: NVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
ms.date: 03/06/2025
ms.topic: language-reference
targetos: Windows
description: Contains information about an asynchronous event that is posted to the Admin Completion Queue in DWord 0 of a Completion Queue Entry. Asynchronous events are used to notify the host software of status, error, and health information.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: NVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST, *PNVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
 - NVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
f1_keywords:
 - PNVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
 - nvme/PNVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
 - NVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
 - nvme/NVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST
dev_langs:
 - c++
---

# NVME_COMPLETION_DW0_ASYNC_EVENT_REQUEST structure

## -description

Contains information about an asynchronous event that is posted to the Admin Completion Queue in DWord 0 of a Completion Queue Entry. Asynchronous events are used to notify the host software of status, error, and health information.

This structure is used in the **DW0** field of the [NVME_COMPLETION_ENTRY](ns-nvme-nvme_completion_entry.md).

## -struct-fields

### -field AsyncEventType

An [NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md) value that indicates the type of the asynchronous event.

More specific information about the event is provided in the Asynchronous Event Information (**AsyncEventInfo**) field.

### -field Reserved0

### -field AsyncEventInfo

Contains detailed information regarding the asynchronous event.

Depending on the value of **AsyncEventType**, this field will contain one of the following values:

- [NVME_ASYNC_EVENT_ERROR_STATUS_CODES](ne-nvme-nvme_async_event_error_status_codes.md)
- [NVME_ASYNC_EVENT_HEALTH_STATUS_CODES](ne-nvme-nvme_async_event_health_status_codes.md)
- [NVME_ASYNC_EVENT_NOTICE_CODES](ne-nvme-nvme_async_event_notice_codes.md)
- [NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md)

### -field LogPage

Indicates the log page associated with the asynchronous event. This log page must be read by the host to clear the event.

### -field Reserved1

## -remarks

## -see-also

- [NVME_CDW11_FEATURE_ASYNC_EVENT_CONFIG](ns-nvme-nvme_cdw11_feature_async_event_config.md)

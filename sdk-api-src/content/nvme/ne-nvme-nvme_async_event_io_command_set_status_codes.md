---
UID: NE:nvme.NVME_ASYNC_EVENT_IO_COMMAND_SET_STATUS_CODES
tech.root: fs
title: NVME_ASYNC_EVENT_IO_COMMAND_SET_STATUS_CODES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate an I/O Command Set event type.
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
 - NVME_ASYNC_EVENT_IO_COMMAND_SET_STATUS_CODES
f1_keywords:
 - NVME_ASYNC_EVENT_IO_COMMAND_SET_STATUS_CODES
 - nvme/NVME_ASYNC_EVENT_IO_COMMAND_SET_STATUS_CODES
dev_langs:
 - c++
---

# NVME_ASYNC_EVENT_IO_COMMAND_SET_STATUS_CODES enumeration


## -description

Contains values that indicate an I/O Command Set event type.

## -enum-fields

### -field NVME_ASYNC_IO_CMD_SET_RESERVATION_LOG_PAGE_AVAILABLE

One or more [Reservation Notification log](ns-nvme-nvme_reservation_notification_log.md) pages are available.

### -field NVME_ASYNC_IO_CMD_SANITIZE_OPERATION_COMPLETED

A sanitize operation has completed without unexpected deallocation of all LBAs.

### -field NVME_ASYNC_IO_CMD_SANITIZE_OPERATION_COMPLETED_WITH_UNEXPECTED_DEALLOCATION 

A sanitize operation has completed with unexpected deallocation of all LBAs and status is available in the Sanitize Status log page.

## -remarks

Values from this enumeration are used in the **NVME_ASYNC_EVENT_TYPE_IO_COMMAND_SET_STATUS** field of the [NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md) enumeration.

## -see-also

[NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md)
[NVME_RESERVATION_NOTIFICATION_LOG](ns-nvme-nvme_reservation_notification_log.md)


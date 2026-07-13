---
UID: NS:nvme.NVME_RESERVATION_NOTIFICATION_LOG
tech.root: fs
title: NVME_RESERVATION_NOTIFICATION_LOG
ms.date: 03/06/2025
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the information in a Reservation Notification Log page.
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
req.typenames: NVME_RESERVATION_NOTIFICATION_LOG, *PNVME_RESERVATION_NOTIFICATION_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_RESERVATION_NOTIFICATION_LOG
 - NVME_RESERVATION_NOTIFICATION_LOG
f1_keywords:
 - PNVME_RESERVATION_NOTIFICATION_LOG
 - nvme/PNVME_RESERVATION_NOTIFICATION_LOG
 - NVME_RESERVATION_NOTIFICATION_LOG
 - nvme/NVME_RESERVATION_NOTIFICATION_LOG
dev_langs:
 - c++
---

# NVME_RESERVATION_NOTIFICATION_LOG structure

## -description

Contains fields that specify the information in a Reservation Notification Log page.

A Reservation Notification log page is created whenever an unmasked reservation notification occurs on any namespace that may be accessed by the controller. The [Get Log Page](ns-nvme-nvme_cdw10_get_log_page.md) command returns a data buffer containing a log page corresponding to a single reservation notification. This log page is global to the controller.

## -struct-fields

### -field LogPageCount

A 64-bit incrementing Reservation Notification log page count, indicating a unique identifier for this notification.

The count starts at `0h` following a controller reset, is incremented with each unique log entry, and rolls over to zero when the maximum count is reached and a log page is created. A value of `0h` indicates an empty log entry.

### -field LogPageType

A [NVME_RESERVATION_NOTIFICATION_TYPES](ne-nvme-nvme_reservation_notification_types.md) value that indicates the Reservation Notification type described by this log page.

### -field AvailableLogPageCount

Indicates the number of additional available Reservation Notification log pages (for example, the number of unread log pages not counting this one).

If there are more than 255 additional available log pages, a value of `255` is returned. A value of zero indicates that there are no additional available log pages.

### -field Reserved0

A reserved field.

### -field NameSpaceId

Indicates the namespace ID of the namespace associated with the Reservation Notification described by this log page.

### -field Reserved1

A reserved field.

## -remarks

## -see-also

- [NVME_RESERVATION_NOTIFICATION_TYPES enumeration](ne-nvme-nvme_reservation_notification_types.md)
- [Get Log Page](ns-nvme-nvme_cdw10_get_log_page.md)

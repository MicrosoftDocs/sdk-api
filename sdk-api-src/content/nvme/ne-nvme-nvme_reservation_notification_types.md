---
UID: NE:nvme.NVME_RESERVATION_NOTIFICATION_TYPES
tech.root: fs
title: NVME_RESERVATION_NOTIFICATION_TYPES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate the type of reservation notification in a Reservation Notification log page.
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
 - NVME_RESERVATION_NOTIFICATION_TYPES
f1_keywords:
 - NVME_RESERVATION_NOTIFICATION_TYPES
 - nvme/NVME_RESERVATION_NOTIFICATION_TYPES
dev_langs:
 - c++
---

# NVME_RESERVATION_NOTIFICATION_TYPES enumeration


## -description

Contains values that indicate the type of reservation notification in a Reservation Notification log page. A Reservation Notification log page is created whenever an unmasked reservation notification occurs on a namespace associated with the controller.

Reservation notifications may be masked from generating a reservation log page on a per reservation notification type and per namespace ID basis through the [Reservation Notification Mask (NVME_FEATURE_NVM_RESERVATION_NOTIFICATION_MASK)](ne-nvme-nvme_features.md) feature.

A host may use the Asynchronous Event Request command to be notified of the presence of one or more available Reservation Notification log pages.

## -enum-fields

### -field NVME_RESERVATION_NOTIFICATION_TYPE_EMPTY_LOG_PAGE

The log page is empty. The Get Log Page command was processed when no unread Reservation Notification log pages were available. All the fields of an empty log page have a value of zero.

### -field NVME_RESERVATION_NOTIFICATION_TYPE_REGISTRATION_PREEMPTED

The registration is preempted.

### -field NVME_RESERVATION_NOTIFICATION_TYPE_REGISTRATION_RELEASED

The reservation is released.

### -field NVME_RESERVATION_NOTIFICATION_TYPE_RESERVATION_PREEPMPTED

The reservation is preempted.

## -remarks

Use this enumeration to specify values in the **NVME_LOG_PAGE_RESERVATION_NOTIFICATION** field of the [NVME_LOG_PAGES](ne-nvme-nvme_log_pages.md) enumeration that is used in the [NVME_ADMIN_COMMAND_GET_LOG_PAGE](ne-nvme-nvme_admin_commands.md) Admin command.

## -see-also


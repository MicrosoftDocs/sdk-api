---
UID: NE:nvme.NVME_LOG_PAGES
tech.root: fs
title: NVME_LOG_PAGES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate the log pages that can be retrieved by the Get Log Page **NVME_ADMIN_COMMAND_GET_LOG_PAGE** Admin Command.
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
 - NVME_LOG_PAGES
f1_keywords:
 - NVME_LOG_PAGES
 - nvme/NVME_LOG_PAGES
dev_langs:
 - c++
---

# NVME_LOG_PAGES enumeration


## -description

Contains values that indicate the log pages that can be retrieved by the Get Log Page **NVME_ADMIN_COMMAND_GET_LOG_PAGE** Admin Command.

## -enum-fields

### -field NVME_LOG_PAGE_ERROR_INFO

The Error Information log page that contains extended error information for a command that completed with an error or reported an error that is not specific to a particular command.

The information contained in the Error Information log page is defined in the [NVME_ERROR_INFO_LOG](ns-nvme-nvme_error_info_log.md) structure.

### -field NVME_LOG_PAGE_HEALTH_INFO

The SMART / Health Information log page that contains SMART and general health information.

The information contained in the SMART/Health Information log page is defined in the [NVME_HEALTH_INFO_LOG](ns-nvme-nvme_health_info_log.md) structure.

### -field NVME_LOG_PAGE_FIRMWARE_SLOT_INFO

The Firmware Slot Information log page that describes the firmware revision stored in each supported firmware slot.

The information contained in the Firmware Slot Information log page is defined in the [FIRMWARE_SLOT_INFO_LOG](ns-nvme-nvme_firmware_slot_info_log.md) structure.

### -field NVME_LOG_PAGE_CHANGED_NAMESPACE_LIST

The Changed Namespace List log page that describes namespaces in the controller that have changed [Identify Namespace](../nvme/ns-nvme-nvme_identify_namespace_data.md) information since the last time the log page was read.

The information contained in the Changed Namespace List log page is defined in the [CHANGED_NAMESPACE_LIST_LOG](ns-nvme-nvme_changed_namespace_list_log.md) structure.

### -field NVME_LOG_PAGE_COMMAND_EFFECTS

The Commands Supported and Effects log page that describes the commands that the controller supports and the effects of those commands on the state of the NVM subsystem.

The information contained in the Commands Supported and Effects log page is defined in the [NVME_COMMAND_EFFECTS_LOG](ns-nvme-nvme_command_effects_log.md) structure.

### -field NVME_LOG_PAGE_DEVICE_SELF_TEST

The Device Self-Test log page that describes the status, completion percentage, and results of a device self-test.

The information contained in the Device Self Test log page is defined in the [NVME_DEVICE_SELF_TEST_LOG](ns-nvme-nvme_device_self_test_log.md) structure.

### -field NVME_LOG_PAGE_TELEMETRY_HOST_INITIATED

The Telemetry Host-Initiated log page that describes telemetry data from the host.

The information contained in the Telemetry Host-Initiated log page is defined in the [NVME_TELEMETRY_HOST_INITIATED_LOG](ns-nvme-nvme_device_self_test_log.md) structure.

### -field NVME_LOG_PAGE_TELEMETRY_CTLR_INITIATED

The Telemetry Controller-Initiated log page that describes telemetry data from the controller.

### -field NVME_LOG_PAGE_RESERVATION_NOTIFICATION

The Reservation Notification log page that is created whenever an unmasked reservation notification occurs on any namespace that may be accessed by the controller.

The information contained in the Reservation Notification log page is defined in the [NVME_RESERVATION_NOTIFICATION_LOG](ns-nvme-nvme_reservation_notification_log.md) structure.

### -field NVME_LOG_PAGE_ENDURANCE_GROUP_INFORMATION

The Endurance Group Information log page that contains information about the amount of data being read from and written to an Endurance Group.

The information contained in the Endurance Group Information log page is defined in the [NVME_ENDURANCE_GROUP_LOG](ns-nvme-nvme_endurance_group_log.md) structure.

### -field NVME_LOG_PAGE_SANITIZE_STATUS

The Sanitize Status log page that is created whenever an unmasked reservation notification occurs on any namespace that may be accessed by the controller.

## -remarks

## -see-also

[NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md)
[NVME_CDW10_GET_LOG_PAGE_V13](ns-nvme-nvme_cdw10_get_log_page_v13.md)


---
UID: NS:nvme.NVME_COMMAND_STATUS
tech.root: fs
title: NVME_COMMAND_STATUS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains information about the status of a command.
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
req.typenames: NVME_COMMAND_STATUS, *PNVME_COMMAND_STATUS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMMAND_STATUS
 - NVME_COMMAND_STATUS
f1_keywords:
 - PNVME_COMMAND_STATUS
 - nvme/PNVME_COMMAND_STATUS
 - NVME_COMMAND_STATUS
 - nvme/NVME_COMMAND_STATUS
dev_langs:
 - c++
---

# NVME_COMMAND_STATUS structure


## -description

Contains information about the status of a command.

This structure is used in the **Status** field of the [NVME_COMPLETION_ENTRY](ns-nvme-nvme_completion_entry.md) and in the **Status** field of the [NVME_ERROR_INFO_LOG](ns-nvme-nvme_error_info_log.md) to indicate the status of a command that has completed.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.P

Indicates whether a Completion Queue entry is a new entry.

The Phase Tag (**P**) values for all Completion Queue entries should be initialized to ‘0’ by the host software prior to setting the **EN** field of the [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) to `1`.

When the controller places an entry in the Completion Queue, it will invert the phase tag to enable host software to identify a new entry. Specifically, for the first set of completion queue entries after **EN** is set to `1`, all Phase Tags are set to `1` when they are posted. For the second set of completion queue entries, when the controller has wrapped around to the top of the Completion Queue, all Phase Tags are cleared to `0` when they are posted. The value of the Phase Tag is inverted on each pass through the Completion Queue.

### -field DUMMYSTRUCTNAME.SC

Indicates a status code identifying any error or status information for the command.

### -field DUMMYSTRUCTNAME.SCT

A [NVME_STATUS_TYPES](ne-nvme-nvme_status_types.md) value that indicates the type of status the controller is returning.

### -field DUMMYSTRUCTNAME.Reserved

### -field DUMMYSTRUCTNAME.M

Indicates whether there is additional status information for the command.

When this value is set to `1`, there is more status information for this command as part of the [Error Information log](ns-nvme-nvme_error_info_log.md) that can be retrieved with the Get Log Page command.

When this value is cleared to `0`, there is no additional status information for this command.

### -field DUMMYSTRUCTNAME.DNR

Indicates whether the command will succeed if it is re-submitted.

When this value is set to `1`, it indicates that if the same command is re-submitted it is expected to fail.

When this value is cleared to `0`, it indicates that the same command may succeed if retried.

If a command is aborted due to a time limited error recovery, this field should be cleared to `0`. If the **SCT** and **SC** fields are cleared to `0h` then this field should be cleared to `0`.

### -field AsUshort

## -remarks

## -see-also

- [NVME_COMPLETION_ENTRY](ns-nvme-nvme_completion_entry.md)
- [NVME_ERROR_INFO_LOG](ns-nvme-nvme_error_info_log.md)


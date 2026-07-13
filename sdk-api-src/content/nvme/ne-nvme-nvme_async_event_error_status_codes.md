---
UID: NE:nvme.NVME_ASYNC_EVENT_ERROR_STATUS_CODES
tech.root: fs
title: NVME_ASYNC_EVENT_ERROR_STATUS_CODES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate a general error event type.
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
 - NVME_ASYNC_EVENT_ERROR_STATUS_CODES
f1_keywords:
 - NVME_ASYNC_EVENT_ERROR_STATUS_CODES
 - nvme/NVME_ASYNC_EVENT_ERROR_STATUS_CODES
dev_langs:
 - c++
---

## -description

Contains values that indicate a general error event type.

## -enum-fields

### -field NVME_ASYNC_ERROR_INVALID_SUBMISSION_QUEUE

A write to an invalid doorbell register. The host software wrote to the doorbell of a queue that was not created.

### -field NVME_ASYNC_ERROR_INVALID_DOORBELL_WRITE_VALUE

Invalid doorbell write value. The host software attempted to write an invalid doorbell value. Some possible causes of this error are:

- The value written was out of range of the corresponding queue’s base address and size.
- The value written is the same as the previously written doorbell value.
- The number of commands that would be added as part of a doorbell write would exceed the number of available entries.
- The host software attempted to add a command to a full Submission Queue.
- The host software attempted to remove a completion queue entry from an empty Completion Queue.

### -field NVME_ASYNC_ERROR_DIAG_FAILURE

A diagnostic failure was detected. This error may include a self-test operation.

### -field NVME_ASYNC_ERROR_PERSISTENT_INTERNAL_DEVICE_ERROR

A failure occurred that is persistent, and the controller is unable to isolate it to a specific set of commands.

If this error is indicated, the Controller Fatal Status (**CFS**) bit of the [NVME_CONTROLLER_STATUS](ns-nvme-nvme_controller_status.md) structure may be set to `1` and the host should perform a reset. For more information, see [NVM Subsystem Reset](ns-nvme-nvme_nvm_subsystem_reset.md).

### -field NVME_ASYNC_ERROR_TRANSIENT_INTERNAL_DEVICE_ERROR

A transient internal error occurred that is specific to a particular set of commands. Controller operation may continue without a reset.

### -field NVME_ASYNC_ERROR_FIRMWARE_IMAGE_LOAD_ERROR

The firmware image could not be loaded. The controller reverted to the previously active firmware image or a baseline read-only firmware image.

## -remarks

Use this enumeration to specify values in the **NVME_ASYNC_EVENT_TYPE_ERROR_STATUS** field of the [NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md) enumeration that is used in the Async Event Request Admin command.

## -see-also

[NVM Subsystem Reset](ns-nvme-nvme_nvm_subsystem_reset.md)
[NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md)
[NVME_ADMIN_COMMANDS](ne-nvme-nvme_admin_commands.md)
[NVME_CONTROLLER_STATUS](ns-nvme-nvme_controller_status.md)


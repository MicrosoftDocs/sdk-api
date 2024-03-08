---
UID: NS:nvme.NVME_CDW11_CREATE_IO_SQ
tech.root: fs
title: NVME_CDW11_CREATE_IO_SQ
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Create IO Submission Queue command, that is used to create IO Submission Queues.
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
req.typenames: NVME_CDW11_CREATE_IO_SQ, *PNVME_CDW11_CREATE_IO_SQ
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_CREATE_IO_SQ
 - NVME_CDW11_CREATE_IO_SQ
f1_keywords:
 - PNVME_CDW11_CREATE_IO_SQ
 - nvme/PNVME_CDW11_CREATE_IO_SQ
 - NVME_CDW11_CREATE_IO_SQ
 - nvme/NVME_CDW11_CREATE_IO_SQ
dev_langs:
 - c++
---

# NVME_CDW11_CREATE_IO_SQ structure


## -description

Contains parameters for the Create IO Submission Queue command, that is used to create IO Submission Queues.

The **NVME_CDW11_CREATE_IO_SQ** structure is used in the **CDW11** field of the **CREATEIOSQ** parameter of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.PC

The Physically Contiguous (PC) field indicates whether the Submission Queue is physically contiguous in memory.

When this value is set to `1`, the Submission Queue is physically contiguous and PRP Entry 1 (**PRP1** in the [Command data structure](ns-nvme-nvme_command.md)) is the address of a contiguous physical buffer. If the value is set to `0`, the Submission Queue is not physically contiguous and **PRP1** is a PRP List pointer.

If this value is cleared to `0` and the Contiguous Queues Required (**CQR**) field is set to `1` in [Controller Capabilities](ns-nvme-nvme_controller_capabilities.md), the controller should return a status of [NVME_STATUS_INVALID_FIELD_IN_COMMAND](ne-nvme-nvme_status_generic_command_codes.md).

If the queue is located in the Controller Memory Buffer and **PC** is cleared to `0`, the controller will fail the command with a status of [NVME_STATUS_INVALID_USE_OF_CONTROLLER_MEMORY_BUFFER](ne-nvme-nvme_status_generic_command_codes.md).

### -field DUMMYSTRUCTNAME.QPRIO

The Queue Priority (QPRIO) field indicates the priority class to use for commands within this Submission Queue by specifying an [NVME_NVM_QUEUE_PRIORITIES](ne-nvme-nvme_nvm_queue_priorities.md) enumeration value.

This field is only used when the weighted round robin with urgent priority class is the arbitration mechanism selected, the field is ignored if weighted round robin with urgent priority class is not used.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.CQID

The Queue Identifier (QID) field indicates the identifier of the Completion Queue to utilize for any command completions entries associated with this Submission Queue.

The value of `0h` (Admin Completion Queue) should not be specified. 

If the value specified is `0h` or does not correspond to a valid I/O Completion Queue, the controller should return an error of [NVME_STATUS_INVALID_QUEUE_IDENTIFIER](ne-nvme-nvme_status_command_specific_codes.md).

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_CREATE_IO_QUEUE](ns-nvme-nvme_cdw10_create_io_queue.md)


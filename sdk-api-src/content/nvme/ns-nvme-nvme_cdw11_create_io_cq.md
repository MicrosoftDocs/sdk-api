---
UID: NS:nvme.NVME_CDW11_CREATE_IO_CQ
tech.root: fs
title: NVME_CDW11_CREATE_IO_CQ
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Create I/O Completion Queue command, that is used to create all I/O Completion Queues with the exception of the Admin Completion Queue.
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
req.typenames: NVME_CDW11_CREATE_IO_CQ, *PNVME_CDW11_CREATE_IO_CQ
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_CREATE_IO_CQ
 - NVME_CDW11_CREATE_IO_CQ
f1_keywords:
 - PNVME_CDW11_CREATE_IO_CQ
 - nvme/PNVME_CDW11_CREATE_IO_CQ
 - NVME_CDW11_CREATE_IO_CQ
 - nvme/NVME_CDW11_CREATE_IO_CQ
dev_langs:
 - c++
---

# NVME_CDW11_CREATE_IO_CQ structure


## -description

Contains parameters for the Create I/O Completion Queue command, that is used to create all I/O Completion Queues with the exception of the Admin Completion Queue.

The **NVME_CDW11_CREATE_IO_CQ** structure is used in the **CDW11** field of the **CREATEIOCQ** parameter of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.PC

The Physically Contiguous (PC) field indicates whether the Completion Queue is physically contiguous in memory.  

When this value is set to `1`, the Completion Queue is physically contiguous and PRP Entry 1 (**PRP1** in the [Command data structure](ns-nvme-nvme_command.md)) is the address of a contiguous physical buffer. If the value is cleared to `0`, the Completion Queue is not physically contiguous and **PRP1** is a PRP List pointer.

If the queue is located in the Controller Memory Buffer and **PC** is cleared to `0`, the controller will fail the command with a status of [NVME_STATUS_INVALID_USE_OF_CONTROLLER_MEMORY_BUFFER](ne-nvme-nvme_status_generic_command_codes.md).

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.IEN

The Interrupts Enabled (IEN) field indicates whether interrupts are enabled for this Completion Queue.

When the value is set to `1`, interrupts are enabled for this Completion Queue. When the value is cleared to `0`, interrupts are disabled for this Completion Queue.

### -field DUMMYSTRUCTNAME.IV

The Interrupt Vector (IV) field indicates the interrupt vector to use for this Completion Queue.

This value corresponds to the Message-signaled interrupt (MSI-X) vector or, if you are using a single message MSI or pin-based interrupts, the value is set to `0h`. In MSI-X, a maximum of 2K vectors are used.

This value should not be set to a value greater than the number of messages the controller supports. If it is, the controller will return a status of [NVME_STATUS_INVALID_INTERRUPT_VECTOR](ne-nvme-nvme_status_command_specific_codes.md).

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_CREATE_IO_QUEUE structure](ns-nvme-nvme_cdw10_create_io_queue.md)


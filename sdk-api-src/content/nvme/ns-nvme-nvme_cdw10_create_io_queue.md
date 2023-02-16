---
UID: NS:nvme.NVME_CDW10_CREATE_IO_QUEUE
tech.root: fs
title: NVME_CDW10_CREATE_IO_QUEUE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters that are used in the Create I/O Completion Queue and Create IO Submission Queue commands.
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
req.typenames: NVME_CDW10_CREATE_IO_QUEUE, *PNVME_CDW10_CREATE_IO_QUEUE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_CREATE_IO_QUEUE
 - NVME_CDW10_CREATE_IO_QUEUE
f1_keywords:
 - PNVME_CDW10_CREATE_IO_QUEUE
 - nvme/PNVME_CDW10_CREATE_IO_QUEUE
 - NVME_CDW10_CREATE_IO_QUEUE
 - nvme/NVME_CDW10_CREATE_IO_QUEUE
dev_langs:
 - c++
---

# NVME_CDW10_CREATE_IO_QUEUE structure


## -description

Contains parameters that are used in the Create I/O Completion Queue and Create IO Submission Queue commands. The Create I/O Completion Queue command is used to create all I/O Completion Queues with the exception of the Admin Completion Queue and the Create I/O Submission Queue command is used to create I/O Submission Queues.

The **NVME_CDW10_CREATE_IO_QUEUE** structure is used in the **CDW10** field of the **CREATEIOCQ** and **CREATEIOSQ** parameters of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.QID

The Queue Identifier (QID) field indicates the identifier to assign to the Completion Queue or Submission Queue to be created.

This identifier corresponds to either the [Completion Queue Head Doorbell](ns-nvme-nvme_completion_queue_head_doorbell.md) used for the Completion Queue command or the [Submission Queue Tail Doorbell](ns-nvme-nvme_submission_queue_tail_doorbell.md) used for the Submission Queue command.

This 16-bit ID value should not exceed the value reported in the [NVME_FEATURE_NUMBER_OF_QUEUES](ne-nvme-nvme_features.md) feature for I/O Completion Queues or I/O Submission Queues. If the value specified is `0h`, exceeds the Number of Queues reported, or corresponds to an identifier already in use, the controller should return an error of [NVME_STATUS_INVALID_QUEUE_IDENTIFIER](ne-nvme-nvme_status_command_specific_codes.md).

### -field DUMMYSTRUCTNAME.QSIZE

The Queue Size (QSIZE) field indicates the size of the Completion Queue or Submission Queue to be created. The Queue Size is indicated in a 16-bit 0’s based field that specifies the number of entries in the queue.

The minimum size for a queue is two entries. The maximum size for either an I/O Submission Queue or an I/O Completion Queue is 64K entries, limited by the maximum queue size supported by the controller that is reported in the Maximum Queue Entries Supported (**MQES**) field of the [NVME_CONTROLLER_CAPABILITIES](ns-nvme-nvme_controller_capabilities.md) structure.

The maximum size for the Admin Submission and Admin Completion Queue is defined as 4K entries. One entry in each queue is not available for use due to Head and Tail entry pointer definition.

If the size is `0h` or larger than the controller supports, the controller should return an error of [Invalid Queue Size](ne-nvme-nvme_status_command_specific_codes.md).

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_CREATE_IO_CQ](ns-nvme-nvme_cdw11_create_io_cq.md)
- [NVME_CDW11_CREATE_IO_SQ](ns-nvme-nvme_cdw11_create_io_sq.md)


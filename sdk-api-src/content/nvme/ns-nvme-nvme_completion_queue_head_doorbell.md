---
UID: NS:nvme.NVME_COMPLETION_QUEUE_HEAD_DOORBELL
tech.root: fs
title: NVME_COMPLETION_QUEUE_HEAD_DOORBELL
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Defines the doorbell register that updates the Head entry pointer for Completion Queue *y*.
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
req.typenames: NVME_COMPLETION_QUEUE_HEAD_DOORBELL, *PNVME_COMPLETION_QUEUE_HEAD_DOORBELL
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMPLETION_QUEUE_HEAD_DOORBELL
 - NVME_COMPLETION_QUEUE_HEAD_DOORBELL
f1_keywords:
 - PNVME_COMPLETION_QUEUE_HEAD_DOORBELL
 - nvme/PNVME_COMPLETION_QUEUE_HEAD_DOORBELL
 - NVME_COMPLETION_QUEUE_HEAD_DOORBELL
 - nvme/NVME_COMPLETION_QUEUE_HEAD_DOORBELL
dev_langs:
 - c++
---

# NVME_COMPLETION_QUEUE_HEAD_DOORBELL structure


## -description

Defines the doorbell register that updates the Head entry pointer for Completion Queue *y*.

The value of *y* is equivalent to the Queue Identifier, the 16-bit ID value that is assigned to the queue when it is created, this value indicates Completion Queue entries that have been processed by host software.

The Offset of the Completion Queue *y* Head Doorbell (CQyHDBL) is: `(1000h + ((2y + 1) * (4 << CAP.DSTRD)))`

Where `CAP.DSTRD` is the value of the **DSTRD** field in [NVME_CONTROLLER_CAPABILITIES](ns-nvme-nvme_controller_capabilities.md).

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.CQH

A Read/Write field that indicates the new value of the Completion Queue Head entry pointer.

This value will overwrite any previously provided Completion Queue Head (**CQH**) value. The difference between the last **CQH** write and the current **CQH** entry pointer write indicates the number of entries that are now available for re-use by the controller in the Completion Queue.

> [!NOTE]
> Completion Queue rollover must be accounted for.

### -field DUMMYSTRUCTNAME.Reserved0

A Read Only reserved field.

### -field AsUlong

## -remarks

The host should not read the doorbell registers. If a doorbell register is read, the value returned is vendor specific. Writing to a non-existent Completion Queue Head Doorbell has undefined results.

Host software should continue to process completion queue entries within Completion Queues regardless of whether there are entries available in any Submission Queue.

## -see-also


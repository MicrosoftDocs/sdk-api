---
UID: NS:nvme.NVME_SUBMISSION_QUEUE_TAIL_DOORBELL
tech.root: fs
title: NVME_SUBMISSION_QUEUE_TAIL_DOORBELL
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Defines the doorbell register that updates the Tail entry pointer for Submission Queue *y*.
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
req.typenames: NVME_SUBMISSION_QUEUE_TAIL_DOORBELL, *PNVME_SUBMISSION_QUEUE_TAIL_DOORBELL
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_SUBMISSION_QUEUE_TAIL_DOORBELL
 - NVME_SUBMISSION_QUEUE_TAIL_DOORBELL
f1_keywords:
 - PNVME_SUBMISSION_QUEUE_TAIL_DOORBELL
 - nvme/PNVME_SUBMISSION_QUEUE_TAIL_DOORBELL
 - NVME_SUBMISSION_QUEUE_TAIL_DOORBELL
 - nvme/NVME_SUBMISSION_QUEUE_TAIL_DOORBELL
dev_langs:
 - c++
---

# NVME_COMPLETION_QUEUE_HEAD_DOORBELL structure


## -description

Defines the doorbell register that updates the Tail entry pointer for Submission Queue *y*.

The value of *y* is equivalent to the Queue Identifier, the 16-bit ID value that is assigned to the queue when it is created, this value indicates to the controller that new commands have been submitted for processing.

The Offset of the Submission Queue *y* Tail Doorbell (CQyHDBL) is: `(1000h + ((2y) * (4 << CAP.DSTRD)))`

Where `CAP.DSTRD` is the value of the **DSTRD** field in [NVME_CONTROLLER_CAPABILITIES](ns-nvme-nvme_controller_capabilities.md).

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.SQT

A Read/Write field that indicates the new value of the Submission Queue Tail entry pointer.

This value will overwrite any previously provided Submission Queue Tail (**SQT**) value. The difference between the last **SQT** write and the current **SQT** write indicates the number of commands added to the Submission Queue.

> [!NOTE]
> Submission Queue rollover must be accounted for.

### -field DUMMYSTRUCTNAME.Reserved0

A Read Only reserved field.

### -field AsUlong

## -remarks

The host should not read the doorbell registers. If a doorbell register is read, the value returned is vendor specific. Writing to a non-existent Submission Queue Tail Doorbell has undefined results.

## -see-also


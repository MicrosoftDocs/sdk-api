---
UID: NS:nvme.NVME_ADMIN_QUEUE_ATTRIBUTES
tech.root: fs
title: NVME_ADMIN_QUEUE_ATTRIBUTES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains the Admin Queue Attributes (AQA) for the Admin Submission Queue and Admin Completion Queue.
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
req.typenames: NVME_ADMIN_QUEUE_ATTRIBUTES, *PNVME_ADMIN_QUEUE_ATTRIBUTES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_ADMIN_QUEUE_ATTRIBUTES
 - NVME_ADMIN_QUEUE_ATTRIBUTES
f1_keywords:
 - PNVME_ADMIN_QUEUE_ATTRIBUTES
 - nvme/PNVME_ADMIN_QUEUE_ATTRIBUTES
 - NVME_ADMIN_QUEUE_ATTRIBUTES
 - nvme/NVME_ADMIN_QUEUE_ATTRIBUTES
dev_langs:
 - c++
---

# NVME_ADMIN_QUEUE_ATTRIBUTES structure


## -description

Contains the Admin Queue Attributes (AQA) for the Admin Submission Queue and Admin Completion Queue.

The Queue Identifier for the Admin Submission Queue and Admin Completion Queue is `0h`. The Admin Submission Queue’s priority is determined by the selected arbitration mechanism. The Admin Submission Queue and Admin Completion Queue are required to be in physically contiguous memory.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.ASQS

Admin Submission Queue Size (ASQS) is a Read/Write field that defines the size of the Admin Submission Queue in entries.

Enabling a controller while this field is cleared to `00h` produces undefined results. The minimum size of the Admin Submission Queue is two entries. The maximum size of the Admin Submission Queue is 4096 entries. This is a 0’s based value.

### -field DUMMYSTRUCTNAME.Reserved0

A Read Only reserved field.

### -field DUMMYSTRUCTNAME.ACQS

Admin Completion Queue Size (ACQS) is a Read/Write field that defines the size of the Admin Completion Queue in entries.

Enabling a controller while this field is cleared to `00h` produces undefined results. The minimum size of the Admin Completion Queue is two entries. The maximum size of the Admin Completion Queue is 4096 entries. This is a 0’s based value.

### -field DUMMYSTRUCTNAME.Reserved1

A Read Only reserved field.

### -field AsUlong

## -remarks

> [!NOTE]
> A Unified Extensible Firmware Interface (UEFI) should be used during boot operations. In low memory environments (like Option ROMs in legacy BIOS environments) there may
> not be sufficient available memory to allocate the necessary Submission and Completion Queues. In these types of conditions, low memory operation of the controller is
> vendor specific.

## -see-also


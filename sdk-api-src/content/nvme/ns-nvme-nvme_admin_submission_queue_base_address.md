---
UID: NS:nvme.NVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
tech.root: fs
title: NVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains the base memory address of the Admin Submission Queue.
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
req.typenames: NVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS, *PNVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
 - NVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
f1_keywords:
 - PNVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
 - nvme/PNVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
 - NVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
 - nvme/NVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS
dev_langs:
 - c++
---

# NVME_ADMIN_SUBMISSION_QUEUE_BASE_ADDRESS structure


## -description

Contains the base memory address of the Admin Submission Queue.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.Reserved0

A Read Only reserved field.

### -field DUMMYSTRUCTNAME.ASQB

Admin Submission Queue Base (ASQB) is a Read/Write field that indicates the 64-bit physical address for the Admin Submission Queue.

This address is memory page aligned based on the value in contiguous [Memory Page Size (**MPS**)](ns-nvme-nvme_controller_configuration.md) units. All Admin commands, including creation of I/O Submission Queues and I/O Completions Queues are submitted to this queue.

### -field AsUlonglong

## -remarks

## -see-also


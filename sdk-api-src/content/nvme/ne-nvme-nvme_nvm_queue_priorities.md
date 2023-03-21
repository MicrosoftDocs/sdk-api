---
UID: NE:nvme.NVME_NVM_QUEUE_PRIORITIES
tech.root: fs
title: NVME_NVM_QUEUE_PRIORITIES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate a priority which can be assigned to an I/O Submission Queue for consideration by an arbitration mechanism if one is supported by the controller.
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
 - NVME_NVM_QUEUE_PRIORITIES
f1_keywords:
 - NVME_NVM_QUEUE_PRIORITIES
 - nvme/NVME_NVM_QUEUE_PRIORITIES
dev_langs:
 - c++
---

# NVME_NVM_QUEUE_PRIORITIES enumeration


## -description

Contains values that indicate a priority which can be assigned to an I/O Submission Queue for consideration by an arbitration mechanism if one is supported by the controller.

If the weighted round robin with urgent priority class arbitration mechanism is supported, then host software may assign a queue priority service class of urgent, high, medium or low. If the weighted round robin with urgent priority class arbitration mechanism is not supported, then the priority setting is not used and is ignored by the controller

## -enum-fields

### -field NVME_NVM_QUEUE_PRIORITY_URGENT

The queue has an urgent priority.

### -field NVME_NVM_QUEUE_PRIORITY_HIGH

The queue has a high priority.

### -field NVME_NVM_QUEUE_PRIORITY_MEDIUM

The queue has a medium priority.

### -field NVME_NVM_QUEUE_PRIORITY_LOW

The queue has a low priority.

## -remarks

Use this enumeration to specify values in the **QPRIO** field of the [NVME_CDW11_CREATE_IO_SQ](ns-nvme-nvme_cdw11_create_io_sq.md) structure that is used in the [Create IO Submission Queue (CREATEIOSQ)](ns-nvme-nvme_command.md) Admin command.

## -see-also

- [NVME_CDW11_CREATE_IO_SQ](ns-nvme-nvme_cdw11_create_io_sq.md)


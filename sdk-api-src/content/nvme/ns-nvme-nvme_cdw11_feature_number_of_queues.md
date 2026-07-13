---
UID: NS:nvme.NVME_CDW11_FEATURE_NUMBER_OF_QUEUES
tech.root: fs
title: NVME_CDW11_FEATURE_NUMBER_OF_QUEUES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Number of Queues Feature that indicate the number of I/O Completion Queues and I/O Submission Queues that the host requests for this controller.
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
req.typenames: NVME_CDW11_FEATURE_NUMBER_OF_QUEUES, *PNVME_CDW11_FEATURE_NUMBER_OF_QUEUES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_NUMBER_OF_QUEUES
 - NVME_CDW11_FEATURE_NUMBER_OF_QUEUES
f1_keywords:
 - PNVME_CDW11_FEATURE_NUMBER_OF_QUEUES
 - nvme/PNVME_CDW11_FEATURE_NUMBER_OF_QUEUES
 - NVME_CDW11_FEATURE_NUMBER_OF_QUEUES
 - nvme/NVME_CDW11_FEATURE_NUMBER_OF_QUEUES
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_NUMBER_OF_QUEUES structure


## -description

Contains parameters for the Number of Queues Feature that indicate the number of I/O Completion Queues and I/O Submission Queues that the host requests for this controller.

The values from this structure are used in the **NumberOfQueues** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.NSQ

Indicates the number of I/O Submission Queues requested by the host. This number does not include the Admin Submission Queue. A minimum of one should be requested, reflecting that the minimum support is for one I/O Submission Queue. This is a 0’s based value.

The maximum value that may be specified is 65,534 (indicating 65,535 I/O Submission Queues).

If the specified value specified is greater than the maximum value, the controller will return a status of [NVME_STATUS_INVALID_FIELD_IN_COMMAND](ne-nvme-nvme_status_generic_command_codes.md).

### -field DUMMYSTRUCTNAME.NCQ

Indicates the number of I/O Completion Queues requested by the host. This number does not include the Admin Completion Queue. A minimum of one should be requested, reflecting that the minimum support is for one I/O Completion Queue. This is a 0’s based value. 

The maximum value that may be specified is 65,534 (indicating 65,535 I/O Completion Queues).

If the specified value specified is greater than the maximum value, the controller will return a status of [NVME_STATUS_INVALID_FIELD_IN_COMMAND](ne-nvme-nvme_status_generic_command_codes.md).

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)


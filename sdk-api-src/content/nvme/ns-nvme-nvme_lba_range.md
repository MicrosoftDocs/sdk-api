---
UID: NS:nvme.NVME_LBA_RANGE
tech.root: fs
title: NVME_LBA_RANGE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters that define a collection of contiguous logical blocks specified by a starting LBA and number of logical blocks.
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
req.typenames: NVME_LBA_RANGE, *PNVME_LBA_RANGE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_LBA_RANGE
 - NVME_LBA_RANGE
f1_keywords:
 - PNVME_LBA_RANGE
 - nvme/PNVME_LBA_RANGE
 - NVME_LBA_RANGE
 - nvme/NVME_LBA_RANGE
dev_langs:
 - c++
---

# NVME_LBA_RANGE structure


## -description

Contains parameters that define a collection of contiguous logical blocks specified by a starting LBA and number of logical blocks.

This structure is used by the Dataset Management command, which provides a list of LBA ranges with optional context attributes. Each LBA range consists of a starting LBA (**StartingLBA**), a length of logical blocks that the range consists of (**LogicalBlockCount**), and the optional context attributes (**Attributes**) to be applied to that range.

## -struct-fields

### -field Attributes

A [NVME_CONTEXT_ATTRIBUTES](ns-nvme-nvme_context_attributes.md) structure that specifies context attributes for the logical block range.

The use of this information is optional and the controller is not required to perform any specific action.

### -field LogicalBlockCount

Specifies the length of the LBA range in logical blocks.

### -field StartingLBA

Specifies the starting logical block in the range.

## -remarks

## -see-also

- [NVME_CDW10_DATASET_MANAGEMENT](ns-nvme-nvme_cdw10_dataset_management.md)
- [NVME_CDW11_DATASET_MANAGEMENT](ns-nvme-nvme_cdw11_dataset_management.md)


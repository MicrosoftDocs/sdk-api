---
UID: NS:nvme.NVME_SET_ATTRIBUTES_ENTRY
tech.root: fs
title: NVME_SET_ATTRIBUTES_ENTRY
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify information for setting an attribute.
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
req.typenames: NVME_SET_ATTRIBUTES_ENTRY, *PNVME_SET_ATTRIBUTES_ENTRY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_SET_ATTRIBUTES_ENTRY
 - NVME_SET_ATTRIBUTES_ENTRY
f1_keywords:
 - PNVME_SET_ATTRIBUTES_ENTRY
 - nvme/PNVME_SET_ATTRIBUTES_ENTRY
 - NVME_SET_ATTRIBUTES_ENTRY
 - nvme/NVME_SET_ATTRIBUTES_ENTRY
dev_langs:
 - c++
---

# NVME_SET_ATTRIBUTES_ENTRY structure


## -description

Contains fields that specify information for setting an attribute.

The **NVM_SET_LIST** structure contains an array of **NVME_SET_ATTRIBUTES_ENTRY** structures.

## -struct-fields

### -field Identifier

Indicates the identifier of the attribute.

### -field ENDGID

### -field Reserved1

A reserved field.

### -field Random4KBReadTypical

### -field OptimalWriteSize

Indicates the optimal write size.

### -field TotalCapacity

Indicates the total capacity.

### -field UnallocatedCapacity

Indicates the unallocated capacity.

### -field Reserved2

## -remarks

## -see-also


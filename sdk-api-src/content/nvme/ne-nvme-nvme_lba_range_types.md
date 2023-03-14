---
UID: NE:nvme.NVME_LBA_RANGE_TYPES
tech.root: fs
title: NVME_LBA_RANGE_TYPES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate the type of Logical Block Addressing (LBA) range in an NVME_LBA_RANGET_TYPE_ENTRY structure.
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
 - NVME_LBA_RANGE_TYPES
f1_keywords:
 - NVME_LBA_RANGE_TYPES
 - nvme/NVME_LBA_RANGE_TYPES
dev_langs:
 - c++
---

# NVME_LBA_RANGE_TYPES enumeration


## -description

Contains values that indicate the type of Logical Block Addressing (LBA) range in an LBA Range Type entry [NVME_LBA_RANGET_TYPE_ENTRY](ns-nvme-nvme_lba_ranget_type_entry.md) structure.

## -enum-fields

### -field NVME_LBA_RANGE_TYPE_RESERVED

The reserved LBA range.

### -field NVME_LBA_RANGE_TYPE_FILESYSTEM

The filesystem LBA range.

### -field NVME_LBA_RANGE_TYPE_RAID

The RAID LBA range.

### -field NVME_LBA_RANGE_TYPE_CACHE

The cache LBA range.

### -field NVME_LBA_RANGE_TYPE_PAGE_SWAP_FILE

The page/swap file LBA range.

## -remarks

LBA range information ise used by a driver to determine if it may utilize a particular LBA range. The information is not exposed to higher level software.

## -see-also

[NVME_LBA_RANGET_TYPE_ENTRY](ns-nvme-nvme_lba_ranget_type_entry.md)


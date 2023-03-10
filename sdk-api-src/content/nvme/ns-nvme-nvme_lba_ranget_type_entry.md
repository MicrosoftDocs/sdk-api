---
UID: NS:nvme.NVME_LBA_RANGET_TYPE_ENTRY
tech.root: fs
title: NVME_LBA_RANGET_TYPE_ENTRY
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters that specify a single entry in a list of Logical Block Address (LBA) ranges, for the LBA Range Type Feature in the Set Features command.
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
req.typenames: NVME_LBA_RANGET_TYPE_ENTRY, *PNVME_LBA_RANGET_TYPE_ENTRY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_LBA_RANGET_TYPE_ENTRY
 - NVME_LBA_RANGET_TYPE_ENTRY
f1_keywords:
 - PNVME_LBA_RANGET_TYPE_ENTRY
 - nvme/PNVME_LBA_RANGET_TYPE_ENTRY
 - NVME_LBA_RANGET_TYPE_ENTRY
 - nvme/NVME_LBA_RANGET_TYPE_ENTRY
dev_langs:
 - c++
---

# NVME_LBA_RANGET_TYPE_ENTRY structure


## -description

Contains parameters that specify a single entry in a list of Logical Block Address (LBA) ranges, for the LBA Range Type Feature in the Set Features command.

## -struct-fields

### -field Type

An [NVME_LBA_RANGE_TYPES](ne-nvme-nvme_lba_range_types.md) value that specifies the type of the LBA range.

### -field Attributes

Specifies attributes for the LBA range. Each bit defines an attribute, as follows:

- Bit 0 - If this bit is set to `1`, the LBA range may be overwritten. If this bit is cleared to `0`, the LBA range should not be overwritten.
- Bit 1 - If this bit is set to `1`, the LBA range should be hidden from the OS/EFI/BIOS. If this bit is cleared to `0`, the area should be visible to the OS/EFI/BIOS.
- Bits 2-7 - Reserved

### -field Attributes.MayOverwritten

### -field Attributes.Hidden

### -field Attributes.Reserved

### -field Attributes.Reserved0

### -field SLBA

Specifies the 64-bit address of the first logical block that is part of this LBA range.

### -field NLB

Specifies the number of logical blocks that are part of this LBA range. This is a 0s based value.

### -field GUID

A Global Unique Identifier (GUID) that uniquely specifies the type of this LBA range. Well known Types may be defined and are published on the [NVM Express website](https://nvmexpress.org/).

### -field Reserved1

## -remarks

## -see-also

- [NVME_CDW11_FEATURE_LBA_RANGE_TYPE](ns-nvme-nvme_cdw11_feature_lba_range_type.md)


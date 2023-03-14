---
UID: NE:nvme.NVME_ACCESS_FREQUENCIES
tech.root: fs
title: NVME_ACCESS_FREQUENCIES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Defines values that indicate the frequency of read and write access to a Logical Block Addressing (LBA) range.
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
 - NVME_ACCESS_FREQUENCIES
f1_keywords:
 - NVME_ACCESS_FREQUENCIES
 - nvme/NVME_ACCESS_FREQUENCIES
dev_langs:
 - c++
---

# NVME_ACCESS_FREQUENCIES enumeration


## -description

Defines values that indicate the frequency of read and write access to a Logical Block Addressing (LBA) range.

## -enum-fields

### -field NVME_ACCESS_FREQUENCY_NONE

No frequency information provided.

### -field NVME_ACCESS_FREQUENCY_TYPICAL

The typical number of reads and writes expected for this LBA range.

### -field NVME_ACCESS_FREQUENCY_INFR_WRITE_INFR_READ

Indicates infrequent writes and infrequent reads to the LBA range.

### -field NVME_ACCESS_FREQUENCY_INFR_WRITE_FR_READ

Indicates infrequent writes and frequent reads to the LBA range.

### -field NVME_ACCESS_FREQUENCY_FR_WRITE_INFR_READ

Indicates frequent writes and infrequent reads to the LBA range.

### -field NVME_ACCESS_FREQUENCY_FR_WRITE_FR_READ

Indicates frequent writes and frequent reads to the LBA range.

### -field NVME_ACCESS_FREQUENCY_ONE_TIME_READ

A one time read. For example, the command is due to a virus scan, backup, file copy, or archive.

### -field NVME_ACCESS_FREQUENCY_SPECULATIVE_READ

A speculative read. The command is part of a prefetch operation.

### -field NVME_ACCESS_FREQUENCY_WILL_BE_OVERWRITTEN

The LBA range is going to be overwritten in the near future.

## -remarks

This enumeration is used to specify values in the **AccessFrequency** field of the [NVME_CDW13_READ_WRITE](ns-nvme-nvme_cdw13_read_write.md) structure and in the **AccessFrequency** field of the [NVME_CONTEXT_ATTRIBUTES](ns-nvme-nvme_context_attributes.md) structure.

## -see-also

[NVME_CDW13_READ_WRITE struct](ns-nvme-nvme_cdw13_read_write.md)


---
UID: NS:nvme.NVME_CONTEXT_ATTRIBUTES
tech.root: fs
title: NVME_CONTEXT_ATTRIBUTES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Specifies optional context attributes for a logical block range (LBA range).
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
req.typenames: NVME_CONTEXT_ATTRIBUTES, *PNVME_CONTEXT_ATTRIBUTES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CONTEXT_ATTRIBUTES
 - NVME_CONTEXT_ATTRIBUTES
f1_keywords:
 - PNVME_CONTEXT_ATTRIBUTES
 - nvme/PNVME_CONTEXT_ATTRIBUTES
 - NVME_CONTEXT_ATTRIBUTES
 - nvme/NVME_CONTEXT_ATTRIBUTES
dev_langs:
 - c++
---

# NVME_CONTEXT_ATTRIBUTES structure


## -description

Specifies optional context attributes for a logical block range (LBA range).

The context attributes specified for each LBA range provides information about how the range is intended to be used by host software. The use of this information is optional and the controller is not required to perform any specific action.

> [!NOTE]
> The controller is required to maintain the integrity of data on the NVM media regardless of whether the attributes provided by host software are accurate.

This structure is used in the **Attributes** field of the [NVME_LBA_RANGE](ns-nvme-nvme_lba_range.md) structure, which is used by the Dataset Management command.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.AccessFrequency

An [NVME_ACCESS_FREQUENCIES](ne-nvme-nvme_access_frequencies.md) value that indicates the access frequency of the LBA range.

### -field DUMMYSTRUCTNAME.AccessLatency

An [NVME_ACCESS_LATENCIES](ne-nvme-nvme_access_latencies.md) value that indicates the access latency of the LBA range.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.SequentialReadRange

Indicates whether the dataset should be optimized for sequential read access.

When this value is set to `1`, the dataset should be optimized for sequential read access. The host expects to perform operations on the dataset as a single object for reads.

### -field DUMMYSTRUCTNAME.SequentialWriteRange

Indicates whether the dataset should be optimized for sequential write access.

When this value is set to `1`, the dataset should be optimized for sequential write access. The host expects to perform operations on the dataset as a single object for writes.

### -field DUMMYSTRUCTNAME.WritePrepare

Indicates whether the specified LBA range is expected to be written in the near future.

When this value is set to `1`, the provided range is expected to be written in the near future.

### -field DUMMYSTRUCTNAME.Reserved1

### -field DUMMYSTRUCTNAME.CommandAccessSize

Specifies the number of logical blocks that are expected to be transferred in a single Read or Write command from this dataset.

A value of `0h` indicates that no Command Access Size is provided.

### -field AsUlong

## -remarks

## -see-also


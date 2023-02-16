---
UID: NS:nvme.NVME_CDW13_READ_WRITE
tech.root: fs
title: NVME_CDW13_READ_WRITE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the NVME Read and NVME Write commands that read or write data and metadata, if applicable, to and from the NVM controller for the specified Logical Block Addresses (LBA).
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
req.typenames: NVME_CDW13_READ_WRITE, *PNVME_CDW13_READ_WRITE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW13_READ_WRITE
 - NVME_CDW13_READ_WRITE
f1_keywords:
 - PNVME_CDW13_READ_WRITE
 - nvme/PNVME_CDW13_READ_WRITE
 - NVME_CDW13_READ_WRITE
 - nvme/NVME_CDW13_READ_WRITE
dev_langs:
 - c++
---

# NVME_CDW13_READ_WRITE structure


## -description

Contains parameters for the NVME Read and NVME Write commands that read or write data and metadata, if applicable, to and from the NVM controller for the specified Logical Block Addresses (LBA).

This structure is used in the **CDW13** parameter of the **READWRITE** field in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.DSM

Indicates attributes for the dataset that the LBAs being read from or written to are associated with.

### -field DUMMYSTRUCTNAME.DSM.AccessFrequency

An [NVME_ACCESS_FREQUENCIES](ne-nvme-nvme_access_frequencies.md) value that specifies the access frequency.

### -field DUMMYSTRUCTNAME.DSM.AccessLatency

An [NVME_ACCESS_LATENCIES](ne-nvme-nvme_access_latencies.md) value that specifies the access latency.

### -field DUMMYSTRUCTNAME.DSM.SequentialRequest

Indicates whether the command is part of a sequential read or write.

For a Read operation, if this value is set to `1`, this command is part of a sequential read that includes multiple Read commands. If the value is cleared to `0`, then no information on sequential access is provided.

For a Write operation, if this value is set to `1`, this command is part of a sequential write that includes multiple Write commands. If the value is cleared to `0`, then no information on sequential access is provided.

### -field DUMMYSTRUCTNAME.DSM.Incompressible

Indicates whether the data is not compressible for the specified logical blocks.

if this value is set to `1`, then data is not compressible for the logical blocks indicated. If the value is cleared to `0`, then no information on compression is provided.

### -field DUMMYSTRUCTNAME.Reserved

### -field DUMMYSTRUCTNAME.DSPEC

A directive specific value.

### -field AsUlong

## -remarks

## -see-also

- [NVME_COMMAND](ns-nvme-nvme_command.md)
- [NVME_CDW12_READ_WRITE](ns-nvme-nvme_cdw12_read_write.md)
- [NVME_CDW15_READ_WRITE](ns-nvme-nvme_cdw15_read_write.md)


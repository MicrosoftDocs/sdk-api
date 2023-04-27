---
UID: NS:nvme.NVME_CDW12_READ_WRITE
tech.root: fs
title: NVME_CDW12_READ_WRITE
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
req.typenames: NVME_CDW12_READ_WRITE, *PNVME_CDW12_READ_WRITE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW12_READ_WRITE
 - NVME_CDW12_READ_WRITE
f1_keywords:
 - PNVME_CDW12_READ_WRITE
 - nvme/PNVME_CDW12_READ_WRITE
 - NVME_CDW12_READ_WRITE
 - nvme/NVME_CDW12_READ_WRITE
dev_langs:
 - c++
---

# NVME_CDW12_READ_WRITE structure


## -description

Contains parameters for the NVME Read and NVME Write commands that read or write data and metadata, if applicable, to and from the NVM controller for the specified Logical Block Addresses (LBA).

This structure is used in the **CDW12** parameter of the **READWRITE** field in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.NLB

Indicates the number of logical blocks to be read or written. This is a 0’s based value.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.DTYPE

A [NVME_DIRECTIVE_TYPES](ne-nvme-nvme_directive_types.md) value that indicates the directive type.

### -field DUMMYSTRUCTNAME.Reserved1

### -field DUMMYSTRUCTNAME.PRINFO

A [NVME_PROTECTION_INFORMATION_TYPES](ne-nvme-nvme_protection_information_types.md) value that specifies the protection information action and check field.

The NVME Read command may specify protection information to be checked as part of the read operation, and the NVME Write command may specify protection information to include as part of a write operation.

### -field DUMMYSTRUCTNAME.FUA

Indicates whether non-volatile media will be read from or written to.

For a Read operation, this value indicates that the data will be returned from non-volatile media.
For a Write operation, this value indicates that the data will be written to non-volatile media before indicating command completion for a write operation.
There is no implied ordering with other commands.

### -field DUMMYSTRUCTNAME.LR

Indicates whether limited retry will be applied.

For a Read operation, if this value is set to `1`, the controller will apply limited retry efforts. If the value is cleared to `0`, the controller will apply all available error recovery means to return the data to the host.

For a Write operation, if this value is set to `1`, the controller will apply limited retry efforts. If the value is cleared to `0`, the controller will apply all available error recovery means to write the data to the Non-Volatile Memory (NVM).

### -field AsUlong

## -remarks

## -see-also

- [NVME_COMMAND](ns-nvme-nvme_command.md)
- [NVME_CDW13_READ_WRITE](ns-nvme-nvme_cdw13_read_write.md)
- [NVME_CDW15_READ_WRITE](ns-nvme-nvme_cdw15_read_write.md)


---
UID: NS:nvme.NVME_CDW15_READ_WRITE
tech.root: fs
title: NVME_CDW15_READ_WRITE
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
req.typenames: NVME_CDW15_READ_WRITE, *PNVME_CDW15_READ_WRITE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW15_READ_WRITE
 - NVME_CDW15_READ_WRITE
f1_keywords:
 - PNVME_CDW15_READ_WRITE
 - nvme/PNVME_CDW15_READ_WRITE
 - NVME_CDW15_READ_WRITE
 - nvme/NVME_CDW15_READ_WRITE
dev_langs:
 - c++
---

# NVME_CDW15_READ_WRITE structure


## -description

Contains parameters for the NVME Read and NVME Write commands that read or write data and metadata, if applicable, to and from the NVM controller for the specified Logical Block Addresses (LBA).

This structure is used in the **CDW15** parameter of the **READWRITE** field in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.ELBAT

Specifies the value of the Logical Block Application Tag.

For a Read operation, this field specifies the expected value of the Logical Block Application Tag.
For a Write operation, This field specifies the Logical Block Application Tag value.

This field is only used if the namespace is formatted to use end-to-end protection information.

### -field DUMMYSTRUCTNAME.ELBATM

Specifies the value of the Logical Block Application Tag Mask.

For a Read operation, this field specifies the expected value of the Logical Block Application Tag Mask.
For a Write operation, This field specifies the Logical Block Application Tag Mask value.

This field is only used if the namespace is formatted to use end-to-end protection information.

### -field AsUlong

## -remarks

## -see-also

- [NVME_COMMAND](ns-nvme-nvme_command.md)
- [NVME_CDW12_READ_WRITE](ns-nvme-nvme_cdw12_read_write.md)
- [NVME_CDW13_READ_WRITE](ns-nvme-nvme_cdw13_read_write.md)


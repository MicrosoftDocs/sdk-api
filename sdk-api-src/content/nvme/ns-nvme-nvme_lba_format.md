---
UID: NS:nvme.NVME_LBA_FORMAT
tech.root: fs
title: NVME_LBA_FORMAT
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters that specify the LBA format to apply to the NVM media as part of the Format NVM command.
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
req.typenames: NVME_LBA_FORMAT, *PNVME_LBA_FORMAT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_LBA_FORMAT
 - NVME_LBA_FORMAT
f1_keywords:
 - PNVME_LBA_FORMAT
 - nvme/PNVME_LBA_FORMAT
 - NVME_LBA_FORMAT
 - nvme/NVME_LBA_FORMAT
dev_langs:
 - c++
---

# NVME_LBA_FORMAT structure


## -description

Contains parameters that specify the LBA format to apply to the NVM media as part of the Format NVM command.

This structure is used in the **LBAF** field of the [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.MS

Indicates the number of metadata bytes provided per LBA based on the value of the LBA Data Size (**LBADS**) field. 

If metadata is not supported, this field will be cleared to `00h`.

If metadata is supported, then the namespace may support the metadata being transferred as part of an extended data LBA or as part of a separate contiguous buffer. If end-to-end data protection is enabled, then the first eight bytes or last eight bytes of the metadata is the protection information.

### -field DUMMYSTRUCTNAME.LBADS

Indicates the supported LBA data size. The value is reported in terms of a power of two (2^n). A value smaller than 9 (for example, 512 bytes) is not supported. If the reported value is `0h`, then the LBA format is not supported or is used.

### -field DUMMYSTRUCTNAME.RP

Indicates the relative performance of the LBA format relative to other LBA formats supported by the controller. Depending on the size of the LBA and associated metadata, there may be performance implications. The performance analysis is based on better performance on a queue depth of 32 with a 4KB read workload. 

The meanings of the values are listed in the following table.

| Value | Definition           |
|-------|----------------------|
| 00b   | Best performance     |
| 01b   | Better performance   |
| 10b   | Good performance     |
| 11b   | Degraded performance |

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md)


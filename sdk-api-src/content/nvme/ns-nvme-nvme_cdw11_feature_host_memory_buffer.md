---
UID: NS:nvme.NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
tech.root: fs
title: NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Host Memory Buffer Feature that provides a mechanism for the host to allocate a portion of host memory for the controller to use exclusively.
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
req.typenames: NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER, *PNVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
 - NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
f1_keywords:
 - PNVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
 - nvme/PNVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
 - NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
 - nvme/NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER structure


## -description

Contains parameters for the Host Memory Buffer Feature that provides a mechanism for the host to allocate a portion of host memory for the controller to use exclusively. 

After a successful completion of a Set Features command that enables the host memory buffer, the host will not write to the associated host memory region, buffer size, or descriptor list until the host memory buffer has been disabled.

After a successful completion of a Set Features command that disables the host memory buffer, the controller will not access any data in the host memory buffer until the host memory buffer has been enabled.

The values from this structure are used in the **HostMemoryBuffer** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.EHM

Enables the host memory buffer.

When this value is set to `1`, the controller may use the host memory buffer. When this value is cleared to `0`, the controller may not use the host memory buffer.

### -field DUMMYSTRUCTNAME.MR

Indicates whether the host will return previously allocated memory to the controller.

When this value is set to `1`, the host will return previously allocated memory the controller that was used prior to a reset or entering the Runtime D3 state. A returned host memory buffer will have the exact same size, descriptor list  address, descriptor list contents, and host memory buffer contents as was last seen by the controller before the **EHM** field was cleared to `0`. If cleared to `0`, the host allocates host memory resources with undefined content.

### -field DUMMYSTRUCTNAME.Reserved

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)
- [NVME_CDW12_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw12_feature_host_memory_buffer.md)
- [NVME_CDW13_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw13_feature_host_memory_buffer.md)
- [NVME_CDW14_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw14_feature_host_memory_buffer.md)
- [NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw15_feature_host_memory_buffer.md)


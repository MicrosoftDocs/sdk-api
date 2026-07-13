---
UID: NS:nvme.NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
tech.root: fs
title: NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
ms.date: 03/06/2025
ms.topic: language-reference
targetos: Windows
description: Defines the parameters of a single entry in the Host Memory Descriptor List.
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
req.typenames: NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY, *PNVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
 - NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
f1_keywords:
 - PNVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
 - nvme/PNVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
 - NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
 - nvme/NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY
dev_langs:
 - c++
---

# NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY structure

## -description

Defines the parameters of a single entry in the Host Memory Descriptor List.

## -struct-fields

### -field BADD

Indicates the host memory address for this entry aligned to the memory page size. the memory page size is defined in the **MPS** field of the [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md).

The lower bits (n:0) of this field indicate that the offset within the memory page is `0h`. For example, if the memory page size is 4KB, then bits 11:00 will be zero; if the memory page size is 8KB, then bits 12:00 will be zero.

### -field BSIZE

Indicates the number of contiguous memory page size **MPS** units for this entry.

### -field Reserved

## -remarks

For a description of the fields and structures that define the Host Memory Descriptor List, see [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md#host-memory-buffer).

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md#host-memory-buffer)
- [NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw11_feature_host_memory_buffer.md)
- [NVME_CDW12_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw12_feature_host_memory_buffer.md)
- [NVME_CDW13_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw13_feature_host_memory_buffer.md)
- [NVME_CDW14_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw14_feature_host_memory_buffer.md)
- [NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw15_feature_host_memory_buffer.md)

---
UID: NS:nvme.NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
tech.root: fs
title: NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains a parameter for the Host Memory Buffer Feature that specifies the number of entries in the Host Memory Descriptor List.
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
req.typenames: NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER, *PNVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
 - NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
f1_keywords:
 - PNVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
 - nvme/PNVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
 - NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
 - nvme/NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER
dev_langs:
 - c++
---

# NVME_CDW15_FEATURE_HOST_MEMORY_BUFFER structure


## -description

Contains a parameter for the Host Memory Buffer Feature that specifies the number of entries in the Host Memory Descriptor List.

This structure are used in the **HostMemoryBuffer** field of the [NVME_CDW15_FEATURES](ns-nvme-nvme_cdw15_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.HMDLEC

Specifies the number of entries in the Host Memory Descriptor List.

The fields for an entry in the Host Memory Descriptor List are specified in the [NVME_HOST_MEMORY_BUFFER_DESCRIPTOR_ENTRY](ns-nvme-nvme_host_memory_buffer_descriptor_entry.md) structure.

### -field AsUlong

## -remarks

For a description of the fields and structures that define the Host Memory Descriptor List, see [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md#host-memory-buffer).

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)
- [NVME_CDW11_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw11_feature_host_memory_buffer.md)
- [NVME_CDW12_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw12_feature_host_memory_buffer.md)
- [NVME_CDW13_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw13_feature_host_memory_buffer.md)
- [NVME_CDW14_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw14_feature_host_memory_buffer.md)


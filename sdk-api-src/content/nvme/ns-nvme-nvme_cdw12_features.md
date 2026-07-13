---
UID: NS:nvme.NVME_CDW12_FEATURES
tech.root: fs
title: NVME_CDW12_FEATURES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Set Features command that sets the attributes of the specified feature.
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
req.typenames: NVME_CDW12_FEATURES, *PNVME_CDW12_FEATURES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW12_FEATURES
 - NVME_CDW12_FEATURES
f1_keywords:
 - PNVME_CDW12_FEATURES
 - nvme/PNVME_CDW12_FEATURES
 - NVME_CDW12_FEATURES
 - nvme/NVME_CDW12_FEATURES
dev_langs:
 - c++
---

# NVME_CDW12_FEATURES structure


## -description

Contains parameters for the Set Features command that sets the attributes of the specified feature.

This structure is used in the **CDW12** parameter of the **SETFEATURES** field in the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field HostMemoryBuffer

Specifies an [NVME_CDW12_FEATURE_HOST_MEMORY_BUFFER](ns-nvme-nvme_cdw12_feature_host_memory_buffer.md) structure containing a value that indicates the size of the host memory buffer.

### -field AsUlong

## -remarks

## -see-also

- [NVME_COMMAND](ns-nvme-nvme_command.md)
- [NVME_CDW10_SET_FEATURES](ns-nvme-nvme_cdw10_set_features.md)
- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)
- [NVME_CDW13_FEATURES](ns-nvme-nvme_cdw13_features.md)
- [NVME_CDW14_FEATURES](ns-nvme-nvme_cdw14_features.md)
- [NVME_CDW15_FEATURES](ns-nvme-nvme_cdw15_features.md)


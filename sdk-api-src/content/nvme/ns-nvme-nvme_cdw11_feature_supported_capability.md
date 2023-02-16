---
UID: NS:nvme.NVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
tech.root: fs
title: NVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that are returned by the Get Features command, which describe the supported capabilities of the specified feature.
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
req.typenames: NVME_CDW11_FEATURE_SUPPORTED_CAPABILITY, *PNVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
 - NVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
f1_keywords:
 - PNVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
 - nvme/PNVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
 - NVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
 - nvme/NVME_CDW11_FEATURE_SUPPORTED_CAPABILITY
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_SUPPORTED_CAPABILITY structure


## -description

Contains values that are returned by the Get Features command, which describe the supported capabilities of the specified feature.

When a Get Features command is submitted with the **SEL** field of the [NVME_CDW10_GET_FEATURES](ns-nvme-nvme_cdw10_get_features.md) structure set to **NVME_FEATURE_VALUE_SUPPORTED_CAPABILITIES**, the **NVME_CDW11_FEATURE_SUPPORTED_CAPABILITY** structure is returned in the **DW0** field of the [Completion Queue Entry](ns-nvme-nvme_completion_entry.md) structure for that command.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.SAVE

Indicates whether the feature is saveable.

When this value is set to `1`, the feature is saveable. 
When this value is set to `0`, the feature is not saveable.

### -field DUMMYSTRUCTNAME.NSS

Indicates whether the feature is namespace specific.

When this value is set to `1`, the feature is namespace specific and settings are applied to individual namespaces.
When this value is set to `0`, the feature is not namespace specific and its settings apply to the entire controller.

### -field DUMMYSTRUCTNAME.MOD

Indicates whether the feature is changeable.

When this value is set to `1`, the feature is changeable.
When this value is set to `0`, the feature is not changeable.

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_GET_FEATURES](ns-nvme-nvme_cdw10_get_features.md)


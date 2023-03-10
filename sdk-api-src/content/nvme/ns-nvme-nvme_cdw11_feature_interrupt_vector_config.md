---
UID: NS:nvme.NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
tech.root: fs
title: NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Interrupt Vector Configuration Feature that configures settings specific to a particular interrupt vector.
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
req.typenames: NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG, *PNVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
 - NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
f1_keywords:
 - PNVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
 - nvme/PNVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
 - NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
 - nvme/NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_INTERRUPT_VECTOR_CONFIG structure


## -description

Contains parameters for the Interrupt Vector Configuration Feature that configures settings specific to a particular interrupt vector.

The values from this structure are used in the **InterruptVectorConfig** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.IV

Indicates the interrupt vector for which the configuration settings are applied.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.CD

Indicates whether interrupt coalescing settings will be applied for the interrupt vector specified in the **IV** field.

When this value is set to `1`, interrupt coalescing settings will not be applied for the interrupt vector specified in the **IV** field. When this value is cleared to `0`, interrupt coalescing settings will apply for the specified interrupt vector.

By default, coalescing settings are enabled for each interrupt vector. Interrupt coalescing is not supported for the Admin Completion Queue.

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)


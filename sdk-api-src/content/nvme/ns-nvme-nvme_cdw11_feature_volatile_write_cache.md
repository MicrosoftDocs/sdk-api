---
UID: NS:nvme.NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
tech.root: fs
title: NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Volatile Write Cache Feature that controls the volatile write cache, if it is supported and present, on the controller.
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
req.typenames: NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE, *PNVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
 - NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
f1_keywords:
 - PNVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
 - nvme/PNVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
 - NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
 - nvme/NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_VOLATILE_WRITE_CACHE structure


## -description

Contains parameters for the Volatile Write Cache Feature that controls the volatile write cache, if it is supported and present, on the controller.

> [!NOTE]
> If the controller is able to guarantee that data present in a write cache is written to non-volatile media on loss of power, then that write cache is considered non-volatile and this setting does not apply to that write cache. In that case, this setting has no effect.

The values from this structure are used in the **VolatileWriteCache** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.WCE

Indicates whether the volatile write cache is enabled.

When this value is set to `1`, the volatile write cache is enabled. When this value is cleared to `0`, the volatile write cache is disabled.

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)


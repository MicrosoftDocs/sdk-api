---
UID: NS:nvme.NVME_CDW11_FEATURE_POWER_MANAGEMENT
tech.root: fs
title: NVME_CDW11_FEATURE_POWER_MANAGEMENT
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values for the Power Management Feature that allows the host to configure the power state.
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
req.typenames: NVME_CDW11_FEATURE_POWER_MANAGEMENT, *PNVME_CDW11_FEATURE_POWER_MANAGEMENT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_POWER_MANAGEMENT
 - NVME_CDW11_FEATURE_POWER_MANAGEMENT
f1_keywords:
 - PNVME_CDW11_FEATURE_POWER_MANAGEMENT
 - nvme/PNVME_CDW11_FEATURE_POWER_MANAGEMENT
 - NVME_CDW11_FEATURE_POWER_MANAGEMENT
 - nvme/NVME_CDW11_FEATURE_POWER_MANAGEMENT
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_POWER_MANAGEMENT structure


## -description

Contains values for the Power Management Feature that allows the host to configure the power state.

The values from this structure are used in the **PowerManagement** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.PS

The Power State (PS) field indicates the new power state into which the controller should transition. 

This power state must one supported by the controller as indicated in the Number of Power States Supported (**NPSS**) field in the [Identify Controller data structure](ns-nvme-nvme_identify_controller_data.md).

If the specified power state is not supported, the controller will return a status of [NVME_STATUS_INVALID_FIELD_IN_COMMAND](ne-nvme-nvme_status_generic_command_codes.md).

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)


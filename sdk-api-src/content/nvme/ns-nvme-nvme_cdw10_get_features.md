---
UID: NS:nvme.NVME_CDW10_GET_FEATURES
tech.root: fs
title: NVME_CDW10_GET_FEATURES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Get Features command that retrieves the attributes of the specified feature.
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
req.typenames: NVME_CDW10_GET_FEATURES, *PNVME_CDW10_GET_FEATURES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_GET_FEATURES
 - NVME_CDW10_GET_FEATURES
f1_keywords:
 - PNVME_CDW10_GET_FEATURES
 - nvme/PNVME_CDW10_GET_FEATURES
 - NVME_CDW10_GET_FEATURES
 - nvme/NVME_CDW10_GET_FEATURES
dev_langs:
 - c++
---

# NVME_CDW10_GET_FEATURES structure


## -description

Contains parameters for the Get Features command that retrieves the attributes of the specified feature.

The Get Features command uses the **NVME_CDW10_GET_FEATURES** structure in the **CDW10** parameter of the **GETFEATURES** field of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.FID

Specifies an [NVME_FEATURES](ne-nvme-nvme_features.md) value that identifies the feature for which to provide data.

### -field DUMMYSTRUCTNAME.SEL

Specifies an [NVME_FEATURE_VALUE_CODES](ne-nvme-nvme_feature_value_codes.md) value that indicates which value of the attributes to return in the provided data.

The controller indicates in bit 4 of the Optional NVM Command Support **ONCS** field of the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure whether the **SEL** field is supported.

If a Get Features command is received with the **SEL** field set to `010b` (**NVME_FEATURE_VALUE_SAVED**), for example, and the controller does not support the Feature Identifier being saved or does not currently have any saved values, then the controller treats the **SEL** field as though it were set to `001b` (**NVME_FEATURE_VALUE_DEFAULT**).

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)


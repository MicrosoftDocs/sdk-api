---
UID: NS:nvme.NVME_CDW10_SET_FEATURES
tech.root: fs
title: NVME_CDW10_SET_FEATURES
ms.date: 08/09/2022
ms.topic: language-reference
targetos: Windows
description: The NVME_CDW10_SET_FEATURES structure contains parameters for the Set Features command that sets the attributes of the specified feature.
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
req.typenames: NVME_CDW10_SET_FEATURES, *PNVME_CDW10_SET_FEATURES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_SET_FEATURES
 - NVME_CDW10_SET_FEATURES
f1_keywords:
 - PNVME_CDW10_SET_FEATURES
 - nvme/PNVME_CDW10_SET_FEATURES
 - NVME_CDW10_SET_FEATURES
 - nvme/NVME_CDW10_SET_FEATURES
dev_langs:
 - c++
---

# NVME_CDW10_SET_FEATURES structure


## -description

Contains parameters for the Set Features command that sets the attributes of the specified feature.

The Set Features command uses the **NVME_CDW10_SET_FEATURES** structure in the **CDW10** parameter of the **SETFEATURES** field of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.FID

Specifies an [NVME_FEATURES](ne-nvme-nvme_features.md) value that identifies the feature for which attributes are being provided.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.SV

Specifies that the controller will save the attribute so that the attribute persists through all power states and resets.

The controller indicates in bit 4 of the Optional NVM Command Support **ONCS** field of the [Identify Controller](ns-nvme-nvme_identify_controller_data.md) data structure whether this field is supported.

If the **FID** specified in the Set Features command is not saveable by the controller and the controller receives a Set Features command with the Save **SV** bit set to one, then the command is aborted with a status of [Feature Identifer Not Saveable **NVME_STATUS_FEATURE_ID_NOT_SAVEABLE**](ne-nvme-nvme_status_command_specific_codes.md).

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)
- [NVME_CDW12_FEATURES](ns-nvme-nvme_cdw12_features.md)
- [NVME_CDW13_FEATURES](ns-nvme-nvme_cdw13_features.md)
- [NVME_CDW14_FEATURES](ns-nvme-nvme_cdw14_features.md)
- [NVME_CDW15_FEATURES](ns-nvme-nvme_cdw15_features.md)


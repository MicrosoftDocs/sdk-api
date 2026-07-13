---
UID: NS:nvme.NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
tech.root: fs
title: NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Autonomous Power State Transition Feature that configures the settings for autonomous power state transitions.
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
req.typenames: NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION, *PNVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
 - NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
f1_keywords:
 - PNVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
 - nvme/PNVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
 - NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
 - nvme/NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION structure


## -description

Contains parameters for the Autonomous Power State Transition Feature that configures the settings for autonomous power state transitions.

The values from this structure are used in the **AutoPowerStateTransition** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.APSTE

Specifies whether the autonomous power state transition is enabled.

When the value of this field is set to `1`, autonomous power state transitions are enabled. When the value of this field is cleared to `0`, autonomous power state transitions are disabled. This field is cleared to `0` by default.

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [NVME_AUTO_POWER_STATE_TRANSITION_ENTRY](ns-nvme-nvme_auto_power_state_transition_entry.md)
- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)


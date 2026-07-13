---
UID: NS:nvme.NVME_AUTO_POWER_STATE_TRANSITION_ENTRY
tech.root: fs
title: NVME_AUTO_POWER_STATE_TRANSITION_ENTRY
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains a 64 bit entry specifying information about idle time and power state transition for each of the allowable 32 power states.
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
req.typenames: NVME_AUTO_POWER_STATE_TRANSITION_ENTRY, *PNVME_AUTO_POWER_STATE_TRANSITION_ENTRY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_AUTO_POWER_STATE_TRANSITION_ENTRY
 - NVME_AUTO_POWER_STATE_TRANSITION_ENTRY
f1_keywords:
 - PNVME_AUTO_POWER_STATE_TRANSITION_ENTRY
 - nvme/PNVME_AUTO_POWER_STATE_TRANSITION_ENTRY
 - NVME_AUTO_POWER_STATE_TRANSITION_ENTRY
 - nvme/NVME_AUTO_POWER_STATE_TRANSITION_ENTRY
dev_langs:
 - c++
---

# NVME_AUTO_POWER_STATE_TRANSITION_ENTRY structure


## -description

Contains a 64 bit entry specifying information about idle time and power state transition for each of the allowable 32 power states. The entries begin with power state 0 and then increase sequentially. For example, power state 0 is described in bytes 7:0, power state 1 is described in bytes 15:8, and so on. The data structure is 256 bytes in size and should be physically contiguous.

For power states that are not supported, the unused **NVME_AUTO_POWER_STATE_TRANSITION_ENTRY** data structure entries will be cleared to all zeroes.

## -struct-fields

### -field Reserved0

Bits 0-2 are reserved.

### -field IdleTransitionPowerState

Idle Transition Power State (ITPS) specified in Bits 3-7 is the non-operational power state for the controller to autonomously transition to after there is a continuous period of idle time in the current power state that exceeds the time specified in the **IdleTimePriorToTransition** field.

### -field IdleTimePriorToTransition

Idle Time Prior to Transition (ITPT) specified in Bits 8-31 is the amount of idle time that occurs in this power state prior to transitioning to the Idle Transition Power State. The time is specified in milliseconds. A value of 0h disables the autonomous power state transition feature for this power state.

### -field Reserved1

Bits 32-63 are reserved.

## -remarks

This structure is used in the Autonomous Power State Transition Enable (**APSTE**) parameter of the [NVME_CDW11_FEATURE_AUTO_POWER_STATE_TRANSITION](ns-nvme-nvme_cdw11_feature_auto_power_state_transition.md) structure.

## -see-also


---
UID: NS:nvme.NVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
tech.root: fs
title: NVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
ms.date: 03/06/2025
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Non-Operational Power State Feature that indicates whether permissive mode is enabled for a non-operational power state.
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
req.typenames: NVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE, *PNVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
 - NVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
f1_keywords:
 - PNVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
 - nvme/PNVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
 - NVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
 - nvme/NVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_NON_OPERATIONAL_POWER_STATE structure

## -description

Contains parameters for the Non-Operational Power State Feature that indicates whether permissive mode is enabled for a non-operational power state.

A power state may be a non-operational power state, as indicated by the **NOPS** field of the [NVME_POWER_STATE_DESC](ns-nvme-nvme_power_state_desc.md) structure that defines the Power State Descriptors in the **PDS** field of the [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md). In a non-operational power state, memory-mapped I/O (MMIO) accesses, configuration register accesses and Admin Queue commands are serviced. No I/O commands are processed by the controller while in a non-operational power state.

When in a non-operational power state, regardless of whether [autonomous power state transitions](ns-nvme-nvme_cdw11_feature_auto_power_state_transition.md) are enabled, the controller will autonomously transition back to the last operational power state when an [I/O Submission Queue Tail Doorbell](ns-nvme-nvme_submission_queue_tail_doorbell.md) is written.

Servicing a memory-mapped I/O (MMIO) or configuration register access may cause the controller power to exceed that advertised by the non-operational power state while the access is being serviced, however, the controller will logically remain in the non-operational power state. Processing a command submitted to the Admin Submission Queue may also cause the controller power to exceed that advertised by the non-operational power state while the command is processed, however, the controller will logically remain in the current power state unless there is an explicit power state transition requested by a Set Features command with the [Power Management](ns-nvme-nvme_cdw11_feature_power_management.md) feature identifier. When servicing a register access or an Admin command, the controller should not exceed the maximum power advertised for the last operational power state.

The values from this structure are used in the **NonOperationalPowerState** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.NOPPME

Specifies whether permissive mode is enabled for a non-operational power state.

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [Power Management](ns-nvme-nvme_cdw11_feature_power_management.md)
- [NVME_POWER_STATE_DESC](ns-nvme-nvme_power_state_desc.md)
- [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md)

---
UID: NE:nvme.NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMITS
tech.root: fs
title: NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMITS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate the command submission and execution recommendations for the associated command.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMITS
f1_keywords:
 - NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMITS
 - nvme/NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMITS
dev_langs:
 - c++
---

# NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMITS enumeration


## -description

Contains values that indicate the command submission and execution recommendations for the associated command.

## -enum-fields

### -field NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMIT_NONE

No command submission or execution restriction.

### -field NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMIT_SINGLE_PER_NAMESPACE

The command may be submitted when there is no other outstanding command to the same namespace and another command should not be submitted to the same namespace until this command is complete.

### -field NVME_COMMAND_EFFECT_SBUMISSION_EXECUTION_LIMIT_SINGLE_PER_CONTROLLER

The command may be submitted when there is no other outstanding command to any namespace and another command should not be submitted to any namespace until this command is complete.

## -remarks

Use the values from this enumeration in the Command Submission and Execution (**CSE**) field of the [NVME_COMMAND_EFFECTS_DATA](ns-nvme-nvme_command_effects_data.md) structure.

## -see-also

[NVME_COMMAND_EFFECTS_DATA](ns-nvme-nvme_command_effects_data.md)


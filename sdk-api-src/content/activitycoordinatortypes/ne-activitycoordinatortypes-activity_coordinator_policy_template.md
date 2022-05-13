---
UID: NE:activitycoordinatortypes._ACTIVITY_COORDINATOR_POLICY_TEMPLATE
tech.root: activity_coordinator
title: ACTIVITY_COORDINATOR_POLICY_TEMPLATE
ms.date: 05/13/2022
targetos: Windows
description: An enumeration of the set of supported template policies.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: activitycoordinatortypes.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - activitycoordinatortypes.h
api_name:
 - _ACTIVITY_COORDINATOR_POLICY_TEMPLATE
 - ACTIVITY_COORDINATOR_POLICY_TEMPLATE
f1_keywords:
 - _ACTIVITY_COORDINATOR_POLICY_TEMPLATE
 - activitycoordinatortypes/_ACTIVITY_COORDINATOR_POLICY_TEMPLATE
 - ACTIVITY_COORDINATOR_POLICY_TEMPLATE
 - activitycoordinatortypes/ACTIVITY_COORDINATOR_POLICY_TEMPLATE
dev_langs:
 - c++
helpviewer_keywords:
 - _ACTIVITY_COORDINATOR_POLICY_TEMPLATE
---

## -description

An enumeration of the set of supported template policies. The configuration for a given template is an internal implementation detail and is subject to change. However, any changes will be carefully considered and would not include changes with the potential to cause significant impact, such as adding major resources like GPU to templates they were previously excluded from. Most changes can be expected to be the careful inclusion of new resource types.

## -enum-fields

### -field ACTIVITY_COORDINATOR_POLICY_TEMPLATE_GOOD

This template policy represents an overall good state of the system and a good time to run an activity, but is not necessarily limited to only good conditions for resources.

Activities run using this policy minimize the likelihood of interference with other programs and user scenarios. Includes, but is not limited to resources such as user-idle, power, CPU, memory, and system disk, but does not consider network or GPU.

| Resource | Available value |
|-----|-----|
| User-Idle | ACTIVITY_COORDINATOR_CONDITION_GOOD |
| Power | ACTIVITY_COORDINATOR_CONDITION_GOOD |
| Network | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| CPU | ACTIVITY_COORDINATOR_CONDITION_GOOD |
| Memory | ACTIVITY_COORDINATOR_CONDITION_GOOD |
| System-Disk | ACTIVITY_COORDINATOR_CONDITION_GOOD |
| GPU | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |

### -field ACTIVITY_COORDINATOR_POLICY_TEMPLATE_MEDIUM

This template policy represents an overall moderate state of the system and a moderate time to run an activity, but is not necessarily limited to only medium conditions for resources.

Activities run using this policy have a moderate likelihood of interference with other programs and user scenarios. Includes, but is not limited to resources such as user-idle, power, CPU, memory, and system disk. It does not consider network or GPU.

| Resource | Available value |
|-----|-----|
| User-Idle | ACTIVITY_COORDINATOR_CONDITION_MEDIUM |
| Power | ACTIVITY_COORDINATOR_CONDITION_MEDIUM |
| Network | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| CPU | ACTIVITY_COORDINATOR_CONDITION_MEDIUM |
| Memory | ACTIVITY_COORDINATOR_CONDITION_MEDIUM |
| System-Disk | ACTIVITY_COORDINATOR_CONDITION_MEDIUM |
| GPU | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |

The resource conditions for this template configuration are more likely to be satisfied than the GOOD template, but the potential to impact other applications is also greater.

### -field ACTIVITY_COORDINATOR_POLICY_TEMPLATE_BASE

This template represents the minimum recommended resource conditions: good user-idle and power with medium CPU, memory, and system disk.

| Resource | Available value |
|-----|-----|
| User-Idle | ACTIVITY_COORDINATOR_CONDITION_GOOD |
| Power | ACTIVITY_COORDINATOR_CONDITION_GOOD |
| Network | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| CPU | ACTIVITY_COORDINATOR_CONDITION_MEDIUM |
| Memory | ACTIVITY_COORDINATOR_CONDITION_MEDIUM |
| System-Disk | ACTIVITY_COORDINATOR_CONDITION_MEDIUM |
| GPU | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |

### -field ACTIVITY_COORDINATOR_POLICY_TEMPLATE_EMPTY

This template represents an empty policy. It is used as the basis for a completely custom policy implementation.

| Resource | Available value |
|-----|-----|
| User-Idle | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| Power | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| Network | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| CPU | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| Memory | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| System-Disk | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |
| GPU | ACTIVITY_COORDINATOR_CONDITION_NOT_SET |

## -remarks

## -see-also

[CreateActivityCoordinatorPolicy](../activitycoordinator/nf-activitycoordinator-createactivitycoordinatorpolicy.md)

[ACTIVITY_COORDINATOR_CONDITION](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_condition.md)

[ACTIVITY_COORDINATOR_RESOURCE](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_resource.md)

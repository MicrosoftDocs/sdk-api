---
UID: NE:activitycoordinatortypes._ACTIVITY_COORDINATOR_RESOURCE
tech.root: activity_coordinator
title: ACTIVITY_COORDINATOR_RESOURCE
ms.date: 05/13/2022
targetos: Windows
description: An enumeration of the set of supported resources.
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
 - _ACTIVITY_COORDINATOR_RESOURCE
 - ACTIVITY_COORDINATOR_RESOURCE
f1_keywords:
 - _ACTIVITY_COORDINATOR_RESOURCE
 - activitycoordinatortypes/_ACTIVITY_COORDINATOR_RESOURCE
 - ACTIVITY_COORDINATOR_RESOURCE
 - activitycoordinatortypes/ACTIVITY_COORDINATOR_RESOURCE
dev_langs:
 - c++
helpviewer_keywords:
 - _ACTIVITY_COORDINATOR_RESOURCE
---

## -description

An enumeration of the set of supported resources.

## -enum-fields

### -field ACTIVITY_COORDINATOR_RESOURCE_USER_IDLE

Represents how actively the user is engaged with the device, and hence how likely activity is to interfere with that use.

### -field ACTIVITY_COORDINATOR_RESOURCE_POWER

Represents the current energy state of the system.

### -field ACTIVITY_COORDINATOR_RESOURCE_NETWORK

Represents the current network state of the system.

### -field ACTIVITY_COORDINATOR_RESOURCE_CPU

Represents the current CPU state of the system.

### -field ACTIVITY_COORDINATOR_RESOURCE_MEMORY

Represents the current memory state of the system.

### -field ACTIVITY_COORDINATOR_RESOURCE_SYSTEM_DISK

Represents the current system-disk state of the system.

System-disk refers to the drive where the operating system is installed.

### -field ACTIVITY_COORDINATOR_RESOURCE_GPU

Represents GPU availability. Includes GPU utilization.

### -field ACTIVITY_COORDINATOR_RESOURCE_NPU

Represents NPU availability. Includes NPU utilization.

## -remarks

### Condition information for resources

| Resource | Good Condition | Medium Condition |
|-----|-----|-----|
| USER_IDLE | User is inactive and/or background activities are highly unlikely to interfere with user experiences. | User may be active. Background activities are unlikely to interfere with highly sensitive experiences. |
| POWER | Energy consumption is highly unlikely to impact user experience. | Energy consumption may impact user experience but will not critically degrade it. Potential impacts may include battery life. |
| NETWORK | Internet access is available; activities highly unlikely to impact user experience. | Internet access is available, but consumption may impact the user. Potential impacts may include consuming limited and/or paid bandwidth. |
| CPU | Additional CPU usage is highly unlikely to interfere with user experiences. | Additional CPU usage may interfere with system performance but will not critically degrade it. |
| MEMORY | Additional memory usage is highly unlikely to interfere with user experiences. | Additional memory usage may interfere with system performance but will not critically degrade it. |
| SYSTEM_DISK | Additional system-disk usage is highly unlikely to interfere with user experiences. | Additional system-disk usage may interfere with system performance but will not critically degrade it. |
| GPU | Additional GPU usage is highly unlikely to interfere with user experiences. | Additional GPU usage may interfere with resource-intensive, visual user experiences such as gaming, video streaming, etc. |
| NPU | Additional NPU usage is highly unlikely to interfere with user experiences. | Additional NPU usage may interfere with user-experiences requiring resource-intensive neural processing tasks. |

> [!NOTE]
> The version of Activity Coordinator that an application compiles with may be different than what is on the system at runtime. Applications should use [IsActivityCoordinatorResourceSupported](../activitycoordinator/nf-activitycoordinator-isactivitycoordinatorresourcesupported.md) to check for Resource support prior to use in APIs.

## -see-also

[GetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-getactivitycoordinatorpolicyresourcecondition.md)

[SetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-setactivitycoordinatorpolicyresourcecondition.md)

[ACTIVITY_COORDINATOR_CONDITION](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_condition.md)

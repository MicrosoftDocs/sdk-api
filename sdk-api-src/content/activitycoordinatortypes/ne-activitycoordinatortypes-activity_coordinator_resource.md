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

An enumeration of the set of supported resources. While the spirit of each resource will remain consistent, the implementation details may change from release to release.

## -enum-fields

### -field ACTIVITY_COORDINATOR_RESOURCE_USER_IDLE

Represents how actively the user is engaged with the device, and hence how likely activity is to interfere with that use. Includes, but isn’t limited to, settings such as game mode, user interactivity, etc.

### -field ACTIVITY_COORDINATOR_RESOURCE_POWER

Represents the current power state of the machine. Includes, but isn’t limited to, battery charge, charging state, thermal constraints, etc.

### -field ACTIVITY_COORDINATOR_RESOURCE_NETWORK

Represents the quality and availability of network connectivity. Includes, but isn’t limited to, internet availability, non-metered network, etc.

### -field ACTIVITY_COORDINATOR_RESOURCE_CPU

Represents CPU availability. Includes CPU utilization, but may also include thermal CPU throttling, etc.

### -field ACTIVITY_COORDINATOR_RESOURCE_MEMORY

Represents Memory availability. Includes Memory utilization, and may include factors like commit charge.

### -field ACTIVITY_COORDINATOR_RESOURCE_SYSTEM_DISK

Represents system drive bandwidth availability. Includes drive utilization.

### -field ACTIVITY_COORDINATOR_RESOURCE_GPU

Represents GPU availability. Includes GPU utilization.

## -remarks

### Condition information for resources

| Resource | Good Condition | Medium Condition |
|-----|-----|-----|
| USER_IDLE | User is inactive and the system is not in game-mode. | The system isn't in game-mode. |
| POWER | The machine is plugged in with sufficient battery power (for applicable systems), and power savings mode is not active. | The machine is plugged in or has sufficient battery reserves. |
| NETWORK | Internet access on a non-metered connection. | Internet access is available. |
| CPU | CPU usage is relatively low. | CPU usage isn't excessively high. |
| MEMORY | The system has low memory pressure. | The system isn't under high memory pressure. |
| SYSTEM_DISK | System-disk usage is relatively low. | System-disk usage isn't excessively high. |
| GPU | GPU usage is relatively low. | GPU usage isn't excessively high. |

## -see-also

[GetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-getactivitycoordinatorpolicyresourcecondition.md)

[SetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-setactivitycoordinatorpolicyresourcecondition.md)

[ACTIVITY_COORDINATOR_CONDITION](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_condition.md)

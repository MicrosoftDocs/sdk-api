---
UID: NE:activitycoordinatortypes._ACTIVITY_COORDINATOR_RESOURCE
tech.root: activity_coordinator
title: ACTIVITY_COORDINATOR_RESOURCE
ms.date: 04/25/2022
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

## -see-also

[GetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-getactivitycoordinatorpolicyresourcecondition.md)

[SetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-setactivitycoordinatorpolicyresourcecondition.md)

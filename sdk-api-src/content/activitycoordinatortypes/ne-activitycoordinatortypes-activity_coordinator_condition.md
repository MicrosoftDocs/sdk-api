---
UID: NE:activitycoordinatortypes._ACTIVITY_COORDINATOR_CONDITION
tech.root: activity_coordinator
title: ACTIVITY_COORDINATOR_CONDITION
ms.date: 04/25/2022
targetos: Windows
description: An enumeration of the set of supported conditions.
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
 - _ACTIVITY_COORDINATOR_CONDITION
 - ACTIVITY_COORDINATOR_CONDITION
f1_keywords:
 - _ACTIVITY_COORDINATOR_CONDITION
 - activitycoordinatortypes/_ACTIVITY_COORDINATOR_CONDITION
 - ACTIVITY_COORDINATOR_CONDITION
 - activitycoordinatortypes/ACTIVITY_COORDINATOR_CONDITION
dev_langs:
 - c++
helpviewer_keywords:
 - _ACTIVITY_COORDINATOR_CONDITION
---

## -description

An enumeration of the set of supported conditions.

## -enum-fields

### -field ACTIVITY_COORDINATOR_CONDITION_GOOD

The condition of the resource is good.

Background activities consuming a resource in this condition are highly unlikely to interfere with user experiences dependent on this resource.

### -field ACTIVITY_COORDINATOR_CONDITION_MEDIUM

The condition of the resource is acceptable.

Background activities consuming a resource in this condition may interfere with user experiences and/or system performance, but will not critically degrade them.

### -field ACTIVITY_COORDINATOR_CONDITION_NOT_SET

The condition of the resource is not monitored.

Policies should only use this condition for resources **not** consumed by their associated activities. Consuming a resource whose condition is not monitored can cause severe impact to the user experience and/or system performance, and may critically degrade them. Potential impacts may also not be transitory, such as consuming network on a metered connection (potential financial cost to the user) or running in a low battery state (reduced battery life for the user who may not have charging access).

## -remarks

## -see-also

[GetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-getactivitycoordinatorpolicyresourcecondition.md)

[SetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-setactivitycoordinatorpolicyresourcecondition.md)

[ACTIVITY_COORDINATOR_RESOURCE](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_resource.md)

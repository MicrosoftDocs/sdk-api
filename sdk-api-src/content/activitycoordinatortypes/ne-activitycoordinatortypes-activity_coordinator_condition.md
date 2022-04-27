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

Increases in use are unlikely to interfere with other work or the resource is highly available.

### -field ACTIVITY_COORDINATOR_CONDITION_MEDIUM

The condition of the resource is acceptable.

Increases in use may interfere with other work or the availability may be subject to constraints. Depending on the use, consumption of the resource may or may not be acceptable. Consuming a resource in medium condition can potentially cause modest impact on other applications leveraging the same resource for high-priority work

### -field ACTIVITY_COORDINATOR_CONDITION_NOT_SET

The condition of the resource is not monitored.

Policies should only use this condition for resources **not** consumed by their associated activities. Consuming a resource whose condition is not monitored can potentially cause a proportionally bad impact on other applications leveraging the same resource for high-priority work. It may also have unintended consequences, such as consuming network on a metered connection (potential financial cost to the user) or running in a low battery state (reduced battery life for the user).

## -remarks

## -see-also

[GetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-getactivitycoordinatorpolicyresourcecondition.md)

[SetActivityCoordinatorPolicyResourceCondition](../activitycoordinator/nf-activitycoordinator-setactivitycoordinatorpolicyresourcecondition.md)

[ACTIVITY_COORDINATOR_RESOURCE](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_resource.md)

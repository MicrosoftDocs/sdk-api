---
UID: NF:activitycoordinator.GetActivityCoordinatorPolicyResourceCondition
tech.root: activity_coordinator
title: GetActivityCoordinatorPolicyResourceCondition
ms.date: 04/25/2022
targetos: Windows
description: Gets a resource’s desired condition for a policy.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: activitycoordinator.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ext-ms-win-resourcemanager-activitycoordinator-l1-1-1.dll
 - ext-ms-win-resourcemanager-activitycoordinator-l1-1-0.dll
 - activitycoordinator.h
api_name:
 - GetActivityCoordinatorPolicyResourceCondition
f1_keywords:
 - GetActivityCoordinatorPolicyResourceCondition
 - activitycoordinator/GetActivityCoordinatorPolicyResourceCondition
dev_langs:
 - c++
helpviewer_keywords:
 - GetActivityCoordinatorPolicyResourceCondition
---

## -description

Gets a resource’s desired condition for a policy. Unmonitored resources in a policy are indicated by **ACTIVITY_COORDINATOR_CONDITION_NOT_SET**.

## -parameters

### -param policy

Supplies a handle to the target policy.

### -param resource

Supplies the resource of interest.

### -param condition

Supplies a pointer to a buffer that receives the resource’s configured condition.

## -returns

Returns an **HRESULT**.

## -remarks

## -see-also

[ACTIVITY_COORDINATOR_CONDITION](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_condition.md)

[ACTIVITY_COORDINATOR_RESOURCE](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_resource.md)

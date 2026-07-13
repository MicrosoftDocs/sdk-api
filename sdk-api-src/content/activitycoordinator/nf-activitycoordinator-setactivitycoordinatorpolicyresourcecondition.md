---
UID: NF:activitycoordinator.SetActivityCoordinatorPolicyResourceCondition
tech.root: activity_coordinator
title: SetActivityCoordinatorPolicyResourceCondition
ms.date: 04/25/2022
targetos: Windows
description: Sets a resource’s desired condition for a policy.
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
req.lib: OneCoreUAP.Lib
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
 - SetActivityCoordinatorPolicyResourceCondition
f1_keywords:
 - SetActivityCoordinatorPolicyResourceCondition
 - activitycoordinator/SetActivityCoordinatorPolicyResourceCondition
dev_langs:
 - c++
helpviewer_keywords:
 - SetActivityCoordinatorPolicyResourceCondition
---

## -description

Sets a resource’s desired condition for a policy. For resources the developer does not want their policy to monitor, they can set the resource’s condition to **ACTIVITY_COORDINATOR_CONDITION_NOT_SET**.

## -parameters

### -param policy

Supplies a handle to the target policy.

### -param resource

Supplies the resource of interest.

### -param condition

Supplies the desired condition.

## -returns

Returns an **HRESULT**.

## -remarks

## -see-also

[ACTIVITY_COORDINATOR_CONDITION](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_condition.md)

[ACTIVITY_COORDINATOR_RESOURCE](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_resource.md)

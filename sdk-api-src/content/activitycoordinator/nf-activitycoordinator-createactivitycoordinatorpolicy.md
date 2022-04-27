---
UID: NF:activitycoordinator.CreateActivityCoordinatorPolicy
tech.root: activity_coordinator
title: CreateActivityCoordinatorPolicy
ms.date: 04/25/2022
targetos: Windows
description: Allocates a new policy and pre-populates fields based on the supplied policy template enumeration.
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
 - 
api_location:
 - activitycoordinator.h
api_name:
 - CreateActivityCoordinatorPolicy
f1_keywords:
 - CreateActivityCoordinatorPolicy
 - activitycoordinator/CreateActivityCoordinatorPolicy
dev_langs:
 - c++
helpviewer_keywords:
 - CreateActivityCoordinatorPolicy
---

## -description

Allocates a new policy and pre-populates fields based on the supplied policy template enumeration. The caller can customize the policy further using [SetActivityCoordinatorPolicyResourceCondition](nf-activitycoordinator-setactivitycoordinatorpolicyresourcecondition.md).

## -parameters

### -param policyTemplate

Supplies a policy template enumeration value.

### -param policy

Supplies a pointer to an **ACTIVITY_COORDINATOR_POLICY** handle that receives the created policy handle.

## -returns

Returns an **HRESULT**.

## -remarks

The caller should subscribe to notifications for the policy opening and closing using [SubscribeActivityCoordinatorPolicy](nf-activitycoordinator-subscribeactivitycoordinatorpolicy.md). Subscriptions listen with an immutable copy of the policy they were created with, allowing the original policy to be safely modified and re-used to create further subscriptions without altering previous subscriptions. When no longer needed, the caller should destroy the policy using [DestroyActivityCoordinatorPolicy](nf-activitycoordinator-destroyactivitycoordinatorpolicy.md).

## -see-also

[SetActivityCoordinatorPolicyResourceCondition](nf-activitycoordinator-setactivitycoordinatorpolicyresourcecondition.md)

[SubscribeActivityCoordinatorPolicy](nf-activitycoordinator-subscribeactivitycoordinatorpolicy.md)

[DestroyActivityCoordinatorPolicy](nf-activitycoordinator-destroyactivitycoordinatorpolicy.md)

[ACTIVITY_COORDINATOR_POLICY_TEMPLATE](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_policy_template.md)

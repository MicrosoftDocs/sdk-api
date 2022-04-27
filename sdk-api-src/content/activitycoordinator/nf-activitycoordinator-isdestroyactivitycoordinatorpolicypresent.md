---
UID: NF:activitycoordinator.IsDestroyActivityCoordinatorPolicyPresent
tech.root: activity_coordinator
title: IsDestroyActivityCoordinatorPolicyPresent
ms.date: 04/26/2022
targetos: Windows
description: Checks if DestroyActivityCoordinatorPolicy is available.
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
 - IsDestroyActivityCoordinatorPolicyPresent
f1_keywords:
 - IsDestroyActivityCoordinatorPolicyPresent
 - activitycoordinator/IsDestroyActivityCoordinatorPolicyPresent
dev_langs:
 - c++
helpviewer_keywords:
 - IsDestroyActivityCoordinatorPolicyPresent
---

## -description

Determines whether or not it's safe to call the [DestroyActivityCoordinatorPolicy](nf-activitycoordinator-destroyactivitycoordinatorpolicy.md) function on the target system. Guard every call to **DestroyActivityCoordinatorPolicy** with a call to **IsDestroyActivityCoordinatorPolicyPresent**.

## -returns

Returns a boolean indicating whether the function is safe to call.

## -remarks

## -see-also

[DestroyActivityCoordinatorPolicy](nf-activitycoordinator-destroyactivitycoordinatorpolicy.md)

---
UID: NF:activitycoordinator.UnsubscribeActivityCoordinatorPolicy
tech.root: activity_coordinator
title: UnsubscribeActivityCoordinatorPolicy
ms.date: 04/25/2022
targetos: Windows
description: Destroys a subscription.
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
 - UnsubscribeActivityCoordinatorPolicy
f1_keywords:
 - UnsubscribeActivityCoordinatorPolicy
 - activitycoordinator/UnsubscribeActivityCoordinatorPolicy
dev_langs:
 - c++
helpviewer_keywords:
 - UnsubscribeActivityCoordinatorPolicy
---

## -description

Destroys a subscription. Note that this routine waits for any in-progress callbacks to return before completing.

> [!CAUTION]
> Do not call the routine from its subscription's callback. Doing so will crash the program.

## -parameters

### -param subscription

Supplies a handle to the target subscription to be destroyed.

## -returns

Returns an **HRESULT**.

## -remarks

## -see-also

[SubscribeActivityCoordinatorPolicy](nf-activitycoordinator-subscribeactivitycoordinatorpolicy.md)

[ACTIVITY_COORDINATOR_CALLBACK](../activitycoordinatortypes/nc-activitycoordinatortypes-activity_coordinator_callback.md)

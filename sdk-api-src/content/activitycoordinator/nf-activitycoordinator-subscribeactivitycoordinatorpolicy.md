---
UID: NF:activitycoordinator.SubscribeActivityCoordinatorPolicy
tech.root: activity_coordinator
title: SubscribeActivityCoordinatorPolicy
ms.date: 04/25/2022
targetos: Windows
description: Creates a subscription that receives notifications for the policy's opening and closing.
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
 - SubscribeActivityCoordinatorPolicy
f1_keywords:
 - SubscribeActivityCoordinatorPolicy
 - activitycoordinator/SubscribeActivityCoordinatorPolicy
dev_langs:
 - c++
helpviewer_keywords:
 - SubscribeActivityCoordinatorPolicy
---

## -description

Creates a subscription that delivers coordination notifications to the supplied callback based on the policy's configuration. Upon notification, the supplied callback is executed with the supplied context. A notification with the current state will be delivered immediately on a separate thread and may be delivered before this call returns. Changes made to the policy after subscribing do not affect the subscription. A single policy can be used to create many subscriptions with unique policy configurations. Notifications are serialized.

## -parameters

### -param policy

Supplies a handle to the target policy.

### -param callback

Supplies the callback to be executed for all coordination notifications from this subscription.

### -param callbackContext

Supplies the context to be passed to callback routine.

### -param subscription

Supplies a pointer to an **ACTIVITY_COORDINATOR_SUBSCRIPTION** handle that receives the created subscription handle.

## -returns

Returns an **HRESULT**.

## -remarks

>**Note** Do not perform your activity in this callback, since it will block delivery of future policy notifications for this subscription. This callback should be used to coordinate the starting and stopping of your activity in response to RUN/STOP notifications from the API.

>**Note** Do not block this callback for extended periods of time, since it will block [UnsubscribeActivityCoordinatorPolicy](nf-activitycoordinator-unsubscribeactivitycoordinatorpolicy.md) and may contribute to thread pool exhaustion.

>**Note** Calls to [UnsubscribeActivityCoordinatorPolicy](nf-activitycoordinator-unsubscribeactivitycoordinatorpolicy.md) from this callback will fail. Unsubscribing must occur outside the callback.

## -see-also

[UnsubscribeActivityCoordinatorPolicy](nf-activitycoordinator-unsubscribeactivitycoordinatorpolicy.md)

[ACTIVITY_COORDINATOR_CALLBACK](../activitycoordinatortypes/nc-activitycoordinatortypes-activity_coordinator_callback.md)

[ACTIVITY_COORDINATOR_NOTIFICATION](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_notification.md)

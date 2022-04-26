---
UID: NC:activitycoordinatortypes.ACTIVITY_COORDINATOR_CALLBACK
tech.root: activity_coordinator
title: ACTIVITY_COORDINATOR_CALLBACK
ms.date: 04/25/2022
targetos: Windows
description: Callback to be called for all notifications for an activity.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: activitycoordinatortypes.h
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
 - LibDef
api_location:
 - activitycoordinatortypes.h
api_name:
 - ACTIVITY_COORDINATOR_CALLBACK
f1_keywords:
 - ACTIVITY_COORDINATOR_CALLBACK
 - activitycoordinatortypes/ACTIVITY_COORDINATOR_CALLBACK
dev_langs:
 - c++
helpviewer_keywords:
 - ACTIVITY_COORDINATOR_CALLBACK
---

## -description

Callback to be called for all notifications for an activity subscription.

## -parameters

### -param notification

Specifies the type of notification for the subscription callback, indicating if the activity should stop or run.

### -param callbackContext

Provides the context that was given when subscribing to the activity.

## -remarks

## -see-also

[SubscribeActivityCoordinatorPolicy](../activitycoordinator/nf-activitycoordinator-subscribeactivitycoordinatorpolicy.md)

[UnsubscribeActivityCoordinatorPolicy](../activitycoordinator/nf-activitycoordinator-unsubscribeactivitycoordinatorpolicy.md)

[ACTIVITY_COORDINATOR_NOTIFICATION](ne-activitycoordinatortypes-activity_coordinator_notification.md)

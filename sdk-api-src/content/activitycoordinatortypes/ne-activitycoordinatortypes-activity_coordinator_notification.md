---
UID: NE:activitycoordinatortypes._ACTIVITY_COORDINATOR_NOTIFICATION
tech.root: activity_coordinator
title: ACTIVITY_COORDINATOR_NOTIFICATION
ms.date: 04/25/2022
targetos: Windows
description: An enumeration of the possible notification types for the subscription callback.
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
 - _ACTIVITY_COORDINATOR_NOTIFICATION
 - ACTIVITY_COORDINATOR_NOTIFICATION
f1_keywords:
 - _ACTIVITY_COORDINATOR_NOTIFICATION
 - activitycoordinatortypes/_ACTIVITY_COORDINATOR_NOTIFICATION
 - ACTIVITY_COORDINATOR_NOTIFICATION
 - activitycoordinatortypes/ACTIVITY_COORDINATOR_NOTIFICATION
dev_langs:
 - c++
helpviewer_keywords:
 - _ACTIVITY_COORDINATOR_NOTIFICATION
---

## -description

An enumeration of the possible notification types for the subscription callback. RUN indicates that the policy is open (it’s resource conditions are satisfied) and the activity should execute; STOP indicates that the policy is closed and the activity should pause execution

## -enum-fields

### -field ACTIVITY_COORDINATOR_NOTIFICATION_RUN

Indicates that it is a good time to do work and therefore, any work that needs to be started or resumed can happen now.

### -field ACTIVITY_COORDINATOR_NOTIFICATION_STOP

Indicates that it is a bad time to do work and therefore, any work that is running should be stopped now.

## -remarks

## -see-also

[ACTIVITY_COORDINATOR_CALLBACK](../activitycoordinatortypes/nc-activitycoordinatortypes-activity_coordinator_callback.md)

[SubscribeActivityCoordinatorPolicy](nf-activitycoordinator-subscribeactivitycoordinatorpolicy.md)

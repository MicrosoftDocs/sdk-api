---
UID: NE:activitycoordinatortypes._ACTIVITY_COORDINATOR_NOTIFICATION
tech.root: activity_coordinator
title: ACTIVITY_COORDINATOR_NOTIFICATION
ms.date: 02/13/2023
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

An enumeration of the possible notification types for the subscription callback.

## -enum-fields

### -field ACTIVITY_COORDINATOR_NOTIFICATION_RUN

Indicates that the conditions of the policy are met, and the associated activity can be started or resumed now.

### -field ACTIVITY_COORDINATOR_NOTIFICATION_STOP

Indicates that the conditions of the policy are _not_ met, and the associated activity should be stopped or paused now.

## -remarks

## -see-also

[ACTIVITY_COORDINATOR_CALLBACK](../activitycoordinatortypes/nc-activitycoordinatortypes-activity_coordinator_callback.md)

[SubscribeActivityCoordinatorPolicy](../activitycoordinator/nf-activitycoordinator-subscribeactivitycoordinatorpolicy.md)

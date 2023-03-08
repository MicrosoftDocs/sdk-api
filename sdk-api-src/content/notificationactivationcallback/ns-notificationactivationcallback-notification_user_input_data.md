---
UID: NS:notificationactivationcallback.NOTIFICATION_USER_INPUT_DATA
title: NOTIFICATION_USER_INPUT_DATA (notificationactivationcallback.h)
description: Contains information about how a user interacted with a notification toast in the action center. This structure is used by Activate.
helpviewer_keywords: ["NOTIFICATION_USER_INPUT_DATA","NOTIFICATION_USER_INPUT_DATA structure","PNOTIFICATION_USER_INPUT_DATA","PNOTIFICATION_USER_INPUT_DATA structure pointer","notificationactivationcallback/NOTIFICATION_USER_INPUT_DATA","notificationactivationcallback/PNOTIFICATION_USER_INPUT_DATA","win32_tile_badge_notif.notification_user_input_data"]
old-location: win32_tile_badge_notif\notification_user_input_data.htm
tech.root: win32_tile_badge_notif
ms.assetid: C39B906E-4EB2-4EFF-B0A3-76E6B17A3662
ms.date: 12/05/2018
ms.keywords: NOTIFICATION_USER_INPUT_DATA, NOTIFICATION_USER_INPUT_DATA structure, PNOTIFICATION_USER_INPUT_DATA, PNOTIFICATION_USER_INPUT_DATA structure pointer, notificationactivationcallback/NOTIFICATION_USER_INPUT_DATA, notificationactivationcallback/PNOTIFICATION_USER_INPUT_DATA, win32_tile_badge_notif.notification_user_input_data
req.header: notificationactivationcallback.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NOTIFICATION_USER_INPUT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NOTIFICATION_USER_INPUT_DATA
 - notificationactivationcallback/NOTIFICATION_USER_INPUT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NotificationActivationCallback.h
api_name:
 - NOTIFICATION_USER_INPUT_DATA
---

# NOTIFICATION_USER_INPUT_DATA structure


## -description



Contains information about how a user interacted with a notification toast in the action center. This structure is used by <a href="/previous-versions/windows/desktop/api/notificationactivationcallback/nf-notificationactivationcallback-inotificationactivationcallback-activate">Activate</a>.

## -struct-fields

### -field Key

The ID of the user input field in the XML payload.

### -field Value

The input value selected by the user for a given input field.

## -remarks

Each key-value pair contains a piece of information based on an item in the notification toast when the <a href="/previous-versions/windows/desktop/api/notificationactivationcallback/nf-notificationactivationcallback-inotificationactivationcallback-activate">Activate</a> callback is triggered.

## -see-also

<a href="/previous-versions/windows/desktop/win32_tile_badge_notif/respond-to-toast-activations">Respond to toast activations</a>
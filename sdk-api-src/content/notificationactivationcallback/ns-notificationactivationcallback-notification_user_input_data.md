---
UID: NS:notificationactivationcallback.NOTIFICATION_USER_INPUT_DATA
title: NOTIFICATION_USER_INPUT_DATA (notificationactivationcallback.h)
author: windows-sdk-content
description: Contains information about how a user interacted with a notification toast in the action center. This structure is used by Activate.
old-location: win32_tile_badge_notif\notification_user_input_data.htm
tech.root: win32_tile_badge_notif
ms.assetid: C39B906E-4EB2-4EFF-B0A3-76E6B17A3662
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NOTIFICATION_USER_INPUT_DATA, NOTIFICATION_USER_INPUT_DATA structure, PNOTIFICATION_USER_INPUT_DATA, PNOTIFICATION_USER_INPUT_DATA structure pointer, notificationactivationcallback/NOTIFICATION_USER_INPUT_DATA, notificationactivationcallback/PNOTIFICATION_USER_INPUT_DATA, win32_tile_badge_notif.notification_user_input_data
ms.topic: struct
f1_keywords: 
 - "notificationactivationcallback/NOTIFICATION_USER_INPUT_DATA"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NotificationActivationCallback.h
api_name:
 - NOTIFICATION_USER_INPUT_DATA
product: Windows
targetos: Windows
req.typenames: NOTIFICATION_USER_INPUT_DATA
req.redist: 
ms.custom: 19H1
---

# NOTIFICATION_USER_INPUT_DATA structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains information about how a user interacted with a notification toast in the action center. This structure is used by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/notificationactivationcallback/nf-notificationactivationcallback-inotificationactivationcallback-activate">Activate</a>.


## -struct-fields




### -field Key

The ID of the user input field in the XML payload.


### -field Value

The input value selected by the user for a given input field.


## -remarks



Each key-value pair contains a piece of information based on an item in the notification toast when the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/notificationactivationcallback/nf-notificationactivationcallback-inotificationactivationcallback-activate">Activate</a> callback is triggered.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/win32_tile_badge_notif/respond-to-toast-activations">Respond to toast activations</a>
 

 


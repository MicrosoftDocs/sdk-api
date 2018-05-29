---
UID: NE:tapi3if.CALL_NOTIFICATION_EVENT
title: CALL_NOTIFICATION_EVENT
author: windows-sdk-content
description: The CALL_NOTIFICATION_EVENT enum describes call notification events. The ITCallNotificationEvent::get_Event method returns a member of this enum to indicate the type of call notification event that occurred.
old-location: tapi3\call_notification_event.htm
old-project: Tapi
ms.assetid: 0c05042f-af1e-4657-bb1c-e6741361b11c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CALL_NOTIFICATION_EVENT, CALL_NOTIFICATION_EVENT enumeration [TAPI 2.2], CNE_MONITOR, CNE_OWNER, _tapi3_call_notification_event, tapi3.call_notification_event, tapi3if/CALL_NOTIFICATION_EVENT, tapi3if/CNE_MONITOR, tapi3if/CNE_OWNER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CALL_NOTIFICATION_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi3if.h
api_name:
-	CALL_NOTIFICATION_EVENT
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CALL_NOTIFICATION_EVENT enumeration


## -description


The 
<b>CALL_NOTIFICATION_EVENT</b> enum describes call notification events. The 
<a href="https://msdn.microsoft.com/08a3925c-e14e-442e-952e-483fc41d049c">ITCallNotificationEvent::get_Event</a> method returns a member of this enum to indicate the type of call notification event that occurred.


## -enum-fields




### -field CNE_OWNER

The current application owns the call on which the event occurred.


### -field CNE_MONITOR

The current application is monitoring the call on which the event occurred.


### -field CNE_LASTITEM




## -see-also




<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>



<a href="https://msdn.microsoft.com/08a3925c-e14e-442e-952e-483fc41d049c">ITCallNotificationEvent::get_Event</a>
 

 


---
UID: NE:tapi3if.CALL_NOTIFICATION_EVENT
title: CALL_NOTIFICATION_EVENT (tapi3if.h)
description: The CALL_NOTIFICATION_EVENT enum describes call notification events. The ITCallNotificationEvent::get_Event method returns a member of this enum to indicate the type of call notification event that occurred.
helpviewer_keywords: ["CALL_NOTIFICATION_EVENT","CALL_NOTIFICATION_EVENT enumeration [TAPI 2.2]","CNE_MONITOR","CNE_OWNER","_tapi3_call_notification_event","tapi3.call_notification_event","tapi3if/CALL_NOTIFICATION_EVENT","tapi3if/CNE_MONITOR","tapi3if/CNE_OWNER"]
old-location: tapi3\call_notification_event.htm
tech.root: tapi3
ms.assetid: 0c05042f-af1e-4657-bb1c-e6741361b11c
ms.date: 12/05/2018
ms.keywords: CALL_NOTIFICATION_EVENT, CALL_NOTIFICATION_EVENT enumeration [TAPI 2.2], CNE_MONITOR, CNE_OWNER, _tapi3_call_notification_event, tapi3.call_notification_event, tapi3if/CALL_NOTIFICATION_EVENT, tapi3if/CNE_MONITOR, tapi3if/CNE_OWNER
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CALL_NOTIFICATION_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALL_NOTIFICATION_EVENT
 - tapi3if/CALL_NOTIFICATION_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALL_NOTIFICATION_EVENT
---

# CALL_NOTIFICATION_EVENT enumeration


## -description

The 
<b>CALL_NOTIFICATION_EVENT</b> enum describes call notification events. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallnotificationevent-get_event">ITCallNotificationEvent::get_Event</a> method returns a member of this enum to indicate the type of call notification event that occurred.

## -enum-fields

### -field CNE_OWNER:0

The current application owns the call on which the event occurred.

### -field CNE_MONITOR

The current application is monitoring the call on which the event occurred.

### -field CNE_LASTITEM

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallnotificationevent-get_event">ITCallNotificationEvent::get_Event</a>

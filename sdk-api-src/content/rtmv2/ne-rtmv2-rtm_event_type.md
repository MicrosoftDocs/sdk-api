---
UID: NE:rtmv2._RTM_EVENT_TYPE
title: RTM_EVENT_TYPE (rtmv2.h)
description: The RTM_EVENT_TYPE enumeration enumerates the events that the routing table manager can notify the client about using the RTM_EVENT_CALLBACK callback.
helpviewer_keywords: ["*PRTM_EVENT_TYPE","PRTM_EVENT_TYPE","PRTM_EVENT_TYPE enumeration pointer [RAS]","RTM_CHANGE_NOTIFICATION","RTM_ENTITY_DEREGISTERED","RTM_ENTITY_REGISTERED","RTM_EVENT_TYPE","RTM_EVENT_TYPE enumeration [RAS]","RTM_ROUTE_EXPIRED","_rtmv2ref_rtm_event_type","rras.rtm_event_type","rtmv2/PRTM_EVENT_TYPE","rtmv2/RTM_CHANGE_NOTIFICATION","rtmv2/RTM_ENTITY_DEREGISTERED","rtmv2/RTM_ENTITY_REGISTERED","rtmv2/RTM_EVENT_TYPE","rtmv2/RTM_ROUTE_EXPIRED"]
old-location: rras\rtm_event_type.htm
tech.root: RRAS
ms.assetid: ea19f59c-8de7-4f52-8029-9775526120c9
ms.date: 12/05/2018
ms.keywords: '*PRTM_EVENT_TYPE, PRTM_EVENT_TYPE, PRTM_EVENT_TYPE enumeration pointer [RAS], RTM_CHANGE_NOTIFICATION, RTM_ENTITY_DEREGISTERED, RTM_ENTITY_REGISTERED, RTM_EVENT_TYPE, RTM_EVENT_TYPE enumeration [RAS], RTM_ROUTE_EXPIRED, _rtmv2ref_rtm_event_type, rras.rtm_event_type, rtmv2/PRTM_EVENT_TYPE, rtmv2/RTM_CHANGE_NOTIFICATION, rtmv2/RTM_ENTITY_DEREGISTERED, rtmv2/RTM_ENTITY_REGISTERED, rtmv2/RTM_EVENT_TYPE, rtmv2/RTM_ROUTE_EXPIRED'
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_EVENT_TYPE
 - rtmv2/_RTM_EVENT_TYPE
 - PRTM_EVENT_TYPE
 - rtmv2/PRTM_EVENT_TYPE
 - RTM_EVENT_TYPE
 - rtmv2/RTM_EVENT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_EVENT_TYPE
---

# RTM_EVENT_TYPE enumeration


## -description

The <b>RTM_EVENT_TYPE</b> enumeration enumerates the events that the routing table manager can notify the client about using the 
<a href="/windows/win32/api/rtmv2/nc-rtmv2-_event_callback">RTM_EVENT_CALLBACK</a> callback.

## -enum-fields

### -field RTM_ENTITY_REGISTERED

A client has just registered with the routing table manager.

### -field RTM_ENTITY_DEREGISTERED

A client has just unregistered.

### -field RTM_ROUTE_EXPIRED

A route has timed out.

### -field RTM_CHANGE_NOTIFICATION

A change notification has been made.

## -see-also

<a href="/windows/win32/api/rtmv2/nc-rtmv2-_event_callback">RTM_EVENT_CALLBACK</a>


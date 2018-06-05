---
UID: NE:rtmv2._RTM_EVENT_TYPE
title: "_RTM_EVENT_TYPE"
author: windows-sdk-content
description: The RTM_EVENT_TYPE enumeration enumerates the events that the routing table manager can notify the client about using the RTM_EVENT_CALLBACK callback.
old-location: rras\rtm_event_type.htm
old-project: RRAS
ms.assetid: ea19f59c-8de7-4f52-8029-9775526120c9
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*PRTM_EVENT_TYPE, PRTM_EVENT_TYPE, PRTM_EVENT_TYPE enumeration pointer [RAS], RTM_CHANGE_NOTIFICATION, RTM_ENTITY_DEREGISTERED, RTM_ENTITY_REGISTERED, RTM_EVENT_TYPE, RTM_EVENT_TYPE enumeration [RAS], RTM_ROUTE_EXPIRED, _RTM_EVENT_TYPE, _rtmv2ref_rtm_event_type, rras.rtm_event_type, rtmv2/PRTM_EVENT_TYPE, rtmv2/RTM_CHANGE_NOTIFICATION, rtmv2/RTM_ENTITY_DEREGISTERED, rtmv2/RTM_ENTITY_REGISTERED, rtmv2/RTM_EVENT_TYPE, rtmv2/RTM_ROUTE_EXPIRED"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rtmv2.h
api_name:
-	RTM_EVENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RTM_EVENT_TYPE enumeration


## -description


The <b>RTM_EVENT_TYPE</b> enumeration enumerates the events that the routing table manager can notify the client about using the 
<a href="https://msdn.microsoft.com/57179cea-d92b-4199-bb61-b34d980532cf">RTM_EVENT_CALLBACK</a> callback.


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




<a href="https://msdn.microsoft.com/57179cea-d92b-4199-bb61-b34d980532cf">RTM_EVENT_CALLBACK</a>
 

 


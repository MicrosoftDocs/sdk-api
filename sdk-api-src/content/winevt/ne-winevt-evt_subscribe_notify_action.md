---
UID: NE:winevt._EVT_SUBSCRIBE_NOTIFY_ACTION
title: EVT_SUBSCRIBE_NOTIFY_ACTION (winevt.h)
author: windows-sdk-content
description: Defines the possible types of data that the subscription service can deliver to your callback.
old-location: wes\evt_subscribe_notify_action.htm
tech.root: wes
ms.assetid: 75166c22-c55c-41b4-8089-ff9a89ddebf5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EVT_SUBSCRIBE_NOTIFY_ACTION, EVT_SUBSCRIBE_NOTIFY_ACTION enumeration [EventLog], EvtSubscribeActionDeliver, EvtSubscribeActionError, wes.evt_subscribe_notify_action, winevt/EVT_SUBSCRIBE_NOTIFY_ACTION, winevt/EvtSubscribeActionDeliver, winevt/EvtSubscribeActionError
ms.topic: enum
f1_keywords: 
 - "winevt/EVT_SUBSCRIBE_NOTIFY_ACTION"
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WinEvt.h
api_name:
 - EVT_SUBSCRIBE_NOTIFY_ACTION
product: Windows
targetos: Windows
req.typenames: EVT_SUBSCRIBE_NOTIFY_ACTION
req.redist: 
ms.custom: 19H1
---

# EVT_SUBSCRIBE_NOTIFY_ACTION enumeration


## -description


Defines the possible types of data that the subscription service can deliver to your callback.


## -enum-fields




### -field EvtSubscribeActionError

Indicates that the <i>Event</i> parameter contains a Win32 error code.


### -field EvtSubscribeActionDeliver

Indicates that the <i>Event</i> parameter contains an event that matches the subscriber's query.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winevt/nc-winevt-evt_subscribe_callback">EVT_SUBSCRIBE_CALLBACK</a>
 

 


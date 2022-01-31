---
UID: NE:winevt._EVT_EVENT_PROPERTY_ID
title: EVT_EVENT_PROPERTY_ID (winevt.h)
description: Defines the values that determine the query information to retrieve.
helpviewer_keywords: ["EVT_EVENT_PROPERTY_ID","EVT_EVENT_PROPERTY_ID enumeration [EventLog]","EvtEventPath","EvtEventPropertyIdEND","EvtEventQueryIDs","wes.evt_subscription_event_property_id","winevt/EVT_EVENT_PROPERTY_ID","winevt/EvtEventPath","winevt/EvtEventPropertyIdEND","winevt/EvtEventQueryIDs"]
old-location: wes\evt_subscription_event_property_id.htm
tech.root: wes
ms.assetid: 19e20da3-5b6b-4f56-b30b-0408695f2267
ms.date: 12/05/2018
ms.keywords: EVT_EVENT_PROPERTY_ID, EVT_EVENT_PROPERTY_ID enumeration [EventLog], EvtEventPath, EvtEventPropertyIdEND, EvtEventQueryIDs, wes.evt_subscription_event_property_id, winevt/EVT_EVENT_PROPERTY_ID, winevt/EvtEventPath, winevt/EvtEventPropertyIdEND, winevt/EvtEventQueryIDs
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
targetos: Windows
req.typenames: EVT_EVENT_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_EVENT_PROPERTY_ID
 - winevt/_EVT_EVENT_PROPERTY_ID
 - EVT_EVENT_PROPERTY_ID
 - winevt/EVT_EVENT_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_EVENT_PROPERTY_ID
---

# EVT_EVENT_PROPERTY_ID enumeration


## -description

Defines the values that determine the query information to retrieve.

## -enum-fields

### -field EvtEventQueryIDs:0

Not supported. The identifier of the query that selected the event. The variant type of this property is EvtVarTypeInt32.

### -field EvtEventPath

The channel or log file from which the event came. The variant type of this property is EvtVarTypeString.

### -field EvtEventPropertyIdEND

This enumeration value marks the end of the enumeration values. It can be used to exit a loop when retrieving all the properties.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgeteventinfo">EvtGetEventInfo</a>

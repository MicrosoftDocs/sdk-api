---
UID: NS:evntcons._EVENT_EXTENDED_ITEM_INSTANCE
title: EVENT_EXTENDED_ITEM_INSTANCE (evntcons.h)
description: Defines the relationship between events if TraceEventInstance was used to log related events.
helpviewer_keywords: ["*PEVENT_EXTENDED_ITEM_INSTANCE","EVENT_EXTENDED_ITEM_INSTANCE","EVENT_EXTENDED_ITEM_INSTANCE structure [ETW]","PEVENT_EXTENDED_ITEM_INSTANCE","PEVENT_EXTENDED_ITEM_INSTANCE structure pointer [ETW]","base.event_extended_item_instance","etw.event_extended_item_instance","evntcons/EVENT_EXTENDED_ITEM_INSTANCE","evntcons/PEVENT_EXTENDED_ITEM_INSTANCE"]
old-location: etw\event_extended_item_instance.htm
tech.root: ETW
ms.assetid: 3def638b-cab2-4b5d-b409-7285caa77ae1
ms.date: 12/05/2018
ms.keywords: '*PEVENT_EXTENDED_ITEM_INSTANCE, EVENT_EXTENDED_ITEM_INSTANCE, EVENT_EXTENDED_ITEM_INSTANCE structure [ETW], PEVENT_EXTENDED_ITEM_INSTANCE, PEVENT_EXTENDED_ITEM_INSTANCE structure pointer [ETW], base.event_extended_item_instance, etw.event_extended_item_instance, evntcons/EVENT_EXTENDED_ITEM_INSTANCE, evntcons/PEVENT_EXTENDED_ITEM_INSTANCE'
req.header: evntcons.h
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
req.typenames: EVENT_EXTENDED_ITEM_INSTANCE, *PEVENT_EXTENDED_ITEM_INSTANCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_EXTENDED_ITEM_INSTANCE
 - evntcons/_EVENT_EXTENDED_ITEM_INSTANCE
 - PEVENT_EXTENDED_ITEM_INSTANCE
 - evntcons/PEVENT_EXTENDED_ITEM_INSTANCE
 - EVENT_EXTENDED_ITEM_INSTANCE
 - evntcons/EVENT_EXTENDED_ITEM_INSTANCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntcons.h
api_name:
 - EVENT_EXTENDED_ITEM_INSTANCE
---

# EVENT_EXTENDED_ITEM_INSTANCE structure (evntcons.h)

## -description

Defines the relationship between events if <a href="/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> was used to log related events.

## -struct-fields

### -field InstanceId

A unique transaction identifier that maps an event to a specific transaction.

### -field ParentInstanceId

A unique transaction identifier of a parent event if you are mapping a hierarchical relationship.

### -field ParentGuid

A GUID that uniquely identifies the provider that logged the event referenced by the <b>ParentInstanceId</b> member.

## -see-also

<a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">EVENT_HEADER_EXTENDED_DATA_ITEM</a>
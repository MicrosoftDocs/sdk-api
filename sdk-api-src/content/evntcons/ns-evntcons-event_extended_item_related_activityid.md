---
UID: NS:evntcons._EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
title: EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID (evntcons.h)
description: Defines the parent event of this event.
helpviewer_keywords: ["*PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID","EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID","EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID structure [ETW]","PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID","PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID structure pointer [ETW]","base.event_extended_item_related_activityid","etw.event_extended_item_related_activityid","evntcons/EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID","evntcons/PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID"]
old-location: etw\event_extended_item_related_activityid.htm
tech.root: ETW
ms.assetid: cabc11ca-e65e-4ffd-9832-7fb4f77417e4
ms.date: 12/05/2018
ms.keywords: '*PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID, EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID, EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID structure [ETW], PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID, PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID structure pointer [ETW], base.event_extended_item_related_activityid, etw.event_extended_item_related_activityid, evntcons/EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID, evntcons/PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID'
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
req.typenames: EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID, *PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
 - evntcons/_EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
 - PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
 - evntcons/PEVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
 - EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
 - evntcons/EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
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
 - EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID
---

# EVENT_EXTENDED_ITEM_RELATED_ACTIVITYID structure (evntcons.h)

## -description

Defines the parent event of this event.

## -struct-fields

### -field RelatedActivityId

A GUID that uniquely identifies the parent activity to which this activity is related. The identifier is specified in the <i>RelatedActivityId</i> parameter passed to the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a> function.

## -see-also

<a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">EVENT_HEADER_EXTENDED_DATA_ITEM</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a>
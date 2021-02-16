---
UID: NS:evntprov._EVENT_DATA_DESCRIPTOR
title: EVENT_DATA_DESCRIPTOR (evntprov.h)
description: Defines one of the data items of the event data.
helpviewer_keywords: ["*PEVENT_DATA_DESCRIPTOR","EVENT_DATA_DESCRIPTOR","EVENT_DATA_DESCRIPTOR structure [ETW]","PEVENT_DATA_DESCRIPTOR","PEVENT_DATA_DESCRIPTOR structure pointer [ETW]","_EVENT_DATA_DESCRIPTOR","base.event_data_descriptor","etw.event_data_descriptor","evntprov/EVENT_DATA_DESCRIPTOR","evntprov/PEVENT_DATA_DESCRIPTOR"]
old-location: etw\event_data_descriptor.htm
tech.root: ETW
ms.assetid: 452ce6f6-3857-4f88-b501-44dd6091b97e
ms.date: 12/05/2018
ms.keywords: '*PEVENT_DATA_DESCRIPTOR, EVENT_DATA_DESCRIPTOR, EVENT_DATA_DESCRIPTOR structure [ETW], PEVENT_DATA_DESCRIPTOR, PEVENT_DATA_DESCRIPTOR structure pointer [ETW], _EVENT_DATA_DESCRIPTOR, base.event_data_descriptor, etw.event_data_descriptor, evntprov/EVENT_DATA_DESCRIPTOR, evntprov/PEVENT_DATA_DESCRIPTOR'
req.header: evntprov.h
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
req.typenames: EVENT_DATA_DESCRIPTOR, *PEVENT_DATA_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_DATA_DESCRIPTOR
 - evntprov/_EVENT_DATA_DESCRIPTOR
 - PEVENT_DATA_DESCRIPTOR
 - evntprov/PEVENT_DATA_DESCRIPTOR
 - EVENT_DATA_DESCRIPTOR
 - evntprov/EVENT_DATA_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntprov.h
api_name:
 - EVENT_DATA_DESCRIPTOR
---

# EVENT_DATA_DESCRIPTOR structure


## -description

The <b>EVENT_DATA_DESCRIPTOR </b> structure defines one of the data items of the event data.

## -struct-fields

### -field Ptr

A pointer to the data.

### -field Size

The size, in bytes, of the data.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Reserved

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Type

Reserved.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Reserved1

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Reserved2

## -remarks

If your event data consists of multiple data items, you would create an array of <b>EVENT_DATA_DESCRIPTOR </b> structures and call the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate">EventDataDescCreate</a> macro to initialize each element with this information. For an example, see <a href="/windows/desktop/ETW/writing-manifest-based-events">Writing Manifest-based Events</a>. 

Note that the total data size of the event (not just this data item) is the lesser of 

<ul>
<li>64 KB</li>
</ul>
And

<ul>
<li>The session's buffer size minus the size of the buffer's header (0x48 bytes) minus the sum of the size of the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a> structure and each extended data item (the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">EVENT_HEADER_EXTENDED_DATA_ITEM</a> structure) that the controller wants to include in the event data.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a>



<a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">EVENT_HEADER_EXTENDED_DATA_ITEM</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate">EventDataDescCreate</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a>



<a href="/windows/desktop/ETW/writing-manifest-based-events">Writing Manifest-based Events</a>
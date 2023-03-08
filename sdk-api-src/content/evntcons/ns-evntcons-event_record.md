---
UID: NS:evntcons._EVENT_RECORD
title: EVENT_RECORD (evntcons.h)
description: The EVENT_RECORD structure (evntcons.h) defines the layout of an event that ETW delivers.
helpviewer_keywords: ["*PEVENT_RECORD","EVENT_RECORD","EVENT_RECORD structure [ETW]","PCEVENT_RECORD","PEVENT_RECORD","PEVENT_RECORD structure pointer [ETW]","_EVENT_RECORD","base.event_record","etw.event_record","relogger/EVENT_RECORD","relogger/PEVENT_RECORD"]
old-location: etw\event_record.htm
tech.root: ETW
ms.assetid: e352c1a7-39a2-43e3-a723-5fc6a3921ee8
ms.date: 08/04/2022
ms.keywords: '*PEVENT_RECORD, EVENT_RECORD, EVENT_RECORD structure [ETW], PCEVENT_RECORD, PEVENT_RECORD, PEVENT_RECORD structure pointer [ETW], _EVENT_RECORD, base.event_record, etw.event_record, relogger/EVENT_RECORD, relogger/PEVENT_RECORD'
req.header: evntcons.h
req.include-header: Evntcons.h
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
req.typenames: EVENT_RECORD, *PEVENT_RECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_RECORD
 - evntcons/_EVENT_RECORD
 - PEVENT_RECORD
 - evntcons/PEVENT_RECORD
 - EVENT_RECORD
 - evntcons/EVENT_RECORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - relogger.h
api_name:
 - EVENT_RECORD
---

# EVENT_RECORD structure (evntcons.h)

## -description

Defines the layout of an event that Event Tracing for Windows (ETW) delivers.

## -struct-fields

### -field EventHeader

Information about the event such as the time stamp for when it was written. For details, see the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a> structure.

### -field BufferContext

Defines information such as the session that logged the event. For details, see the <a href="/windows/desktop/api/relogger/ns-relogger-etw_buffer_context">ETW_BUFFER_CONTEXT</a> structure.

### -field ExtendedDataCount

The number of extended data structures in the <b>ExtendedData</b> member.

### -field UserDataLength

The size, in bytes, of the data in the <b>UserData</b> member.

### -field ExtendedData

One or more extended data items that ETW collects.  The extended data includes some items, such as the security identifier (SID) of the user that logged the event, only if the controller sets the <i>EnableProperty</i> parameter passed to the <a href="/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> or <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function. The extended data includes other items, such as the related activity identifier and decoding information for trace logging, regardless whether the controller sets the <i>EnableProperty</i> parameter passed to  <b>EnableTraceEx</b> or <b>EnableTraceEx2</b>.  For details, see the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">EVENT_HEADER_EXTENDED_DATA_ITEM</a> structure .

### -field UserData

Event specific data. To parse this data, see <a href="/windows/desktop/ETW/retrieving-event-data-using-tdh">Retrieving Event Data Using TDH</a>. If the <b>Flags</b> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a> contains  <b>EVENT_HEADER_FLAG_STRING_ONLY</b>, the data is a null-terminated Unicode string that you do not need TDH to parse.

### -field UserContext

Th context specified in the <b>Context</b> member of the <a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a> structure that is passed to the <a href="/windows/desktop/ETW/opentrace">OpenTrace</a> function.

## -remarks

The <b>EVENT_RECORD</b> structure is passed to the consumer's implementation of the <a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> callback .

## -see-also

<a href="/windows/desktop/api/relogger/ns-relogger-etw_buffer_context">ETW_BUFFER_CONTEXT</a>



<a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a>



<a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">EVENT_HEADER_EXTENDED_DATA_ITEM</a>



<a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a>



<a href="/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a>



<a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>



<a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a>



<a href="/windows/desktop/ETW/opentrace">OpenTrace</a>

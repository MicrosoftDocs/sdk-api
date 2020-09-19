---
UID: NC:evntrace.PEVENT_TRACE_BUFFER_CALLBACKA
title: PEVENT_TRACE_BUFFER_CALLBACKA (evntrace.h)
description: Consumers implement this function to receive statistics about each buffer of events that ETW delivers to an event trace consumer.
helpviewer_keywords: ["BufferCallback","BufferCallback callback function [ETW]","PEVENT_TRACE_BUFFER_CALLBACK","PEVENT_TRACE_BUFFER_CALLBACK callback","PEVENT_TRACE_BUFFER_CALLBACKA","PEVENT_TRACE_BUFFER_CALLBACKW","_evt_buffercallback","base.buffercallback","etw.buffercallback","evntrace/BufferCallback"]
old-location: etw\buffercallback.htm
tech.root: ETW
ms.assetid: 0cfe2f62-63dc-45a6-96ce-fb4bf458358f
ms.date: 12/05/2018
ms.keywords: BufferCallback, BufferCallback callback function [ETW], PEVENT_TRACE_BUFFER_CALLBACK, PEVENT_TRACE_BUFFER_CALLBACK callback, PEVENT_TRACE_BUFFER_CALLBACKA, PEVENT_TRACE_BUFFER_CALLBACKW, _evt_buffercallback, base.buffercallback, etw.buffercallback, evntrace/BufferCallback
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PEVENT_TRACE_BUFFER_CALLBACKA
 - evntrace/PEVENT_TRACE_BUFFER_CALLBACKA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Evntrace.h
api_name:
 - BufferCallback
 - pevent_trace_buffer_callbacka
---

## -description

Consumers implement this function to  receive statistics about each buffer of events that ETW delivers to an event trace consumer. ETW calls this function after the events for each buffer are delivered.

The <b>PEVENT_TRACE_BUFFER_CALLBACK</b> type defines a pointer to this callback function. <b>BufferCallback</b> is a placeholder for the application-defined function name.

## -parameters

### -param Logfile

Pointer to an <a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a> structure that contains information about the buffer.

## -returns

To continue processing events, return <b>TRUE</b>. Otherwise, return <b>FALSE</b>.
Returning <b>FALSE</b> will terminate the <a href="/windows/desktop/ETW/processtrace">ProcessTrace</a> function.

## -remarks

To specify the function that ETW calls to deliver the buffer statistics, set the 
<b>BufferCallback</b> member of the 
<a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a> structure that you pass to the 
<a href="/windows/desktop/ETW/opentrace">OpenTrace</a> function.

## Examples

For an example implementation of a 
<b>BufferCallback</b> function, see 
<a href="/windows/desktop/ETW/retrieving-event-data-using-mof">Retrieving Event Data Using MOF</a>.

<div class="code"></div>

> [!NOTE]
> The evntrace.h header defines PEVENT_TRACE_BUFFER_CALLBACK as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a>

<a href="/windows/desktop/ETW/processtrace">ProcessTrace</a>

---
UID: NF:evntcons.GetEventProcessorIndex
tech.root: ETW
title: GetEventProcessorIndex (evntcons.h)
ms.date: 10/21/2024
ms.keywords: GetEventProcessorIndex
targetos: Windows
description: 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: evntcons.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntcons.h
api_name:
 - GetEventProcessorIndex
f1_keywords:
 - GetEventProcessorIndex
 - evntcons/GetEventProcessorIndex
dev_langs:
 - c++
helpviewer_keywords:
 - GetEventProcessorIndex
---

# GetEventProcessorIndex function (evntcons.h)

## -description

Retrieves the Event Processor index.

## -parameters

### -param EventRecord

The [EVENT_RECORD](/windows/win32/api/evntcons/ns-evntcons-event_record).

## -returns

Returns the **ProcessorIndex** or **ProcessorNumber** from the [ETW_BUFFER_CONTEXT](/windows/win32/api/evntrace/ns-evntrace-etw_buffer_context) **BufferContext** member of the provided _EventRecord_.

## -remarks

## -see-also


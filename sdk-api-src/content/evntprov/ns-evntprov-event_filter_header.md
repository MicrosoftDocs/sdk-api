---
UID: NS:evntprov._EVENT_FILTER_HEADER
title: EVENT_FILTER_HEADER (evntprov.h)
description:
  Defines the header data that must precede the filter data that is defined in
  the instrumentation manifest.
helpviewer_keywords:
  [
    "*PEVENT_FILTER_HEADER",
    "EVENT_FILTER_HEADER",
    "EVENT_FILTER_HEADER structure [ETW]",
    "PEVENT_FILTER_HEADER",
    "PEVENT_FILTER_HEADER structure pointer [ETW]",
    "etw.event_filter_header",
    "evntprov/EVENT_FILTER_HEADER",
    "evntprov/PEVENT_FILTER_HEADER",
  ]
old-location: etw\event_filter_header.htm
tech.root: ETW
ms.assetid: 364a253d-f4c4-494a-af43-487c70912542
ms.date: 12/05/2018
ms.keywords:
  "*PEVENT_FILTER_HEADER, EVENT_FILTER_HEADER, EVENT_FILTER_HEADER structure
  [ETW], PEVENT_FILTER_HEADER, PEVENT_FILTER_HEADER structure pointer [ETW],
  etw.event_filter_header, evntprov/EVENT_FILTER_HEADER,
  evntprov/PEVENT_FILTER_HEADER"
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: EVENT_FILTER_HEADER, *PEVENT_FILTER_HEADER
req.redist:
ms.custom: 19H1
f1_keywords:
  - _EVENT_FILTER_HEADER
  - evntprov/_EVENT_FILTER_HEADER
  - PEVENT_FILTER_HEADER
  - evntprov/PEVENT_FILTER_HEADER
  - EVENT_FILTER_HEADER
  - evntprov/EVENT_FILTER_HEADER
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
  - EVENT_FILTER_HEADER
---

# EVENT_FILTER_HEADER structure

## -description

Defines the header data that must precede the filter data that is defined in the
instrumentation manifest.

## -struct-fields

### -field Id

The identifier that identifies the filter in the manifest for a schematized
filter. The **value** attribute of the **filter** element contains the
identifier.

### -field Version

The version number of the filter for a schematized filter. The **version**
attribute of the **filter** element contains the version number.

### -field Reserved

Reserved

### -field InstanceId

An identifier that identifies the session that passed the filter. ETW sets this
value; the session must set this member to zero.

Providers use this value to set the _Filter_ parameter of
[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex) to
prevent the event from being written to the session if the event data does not
match the filter criteria (the provider determines the semantics of how the
filter data is used in determining whether the event is written to the session).

### -field Size

The size, in bytes, of this header and the filter data that is appended to the
end of this header.

### -field NextOffset

The offset from the beginning of this filter object to the next filter object.
The value is zero if there are no more filter blocks. ETW sets this value; the
session must set this member to zero.

## -remarks

The filter data that you pass to the provider also includes a header. The
following shows an example of how you would define a filter that contained three
integers:

```c
struct _MY_FILTER {
    EVENT_FILTER_HEADER FilterHeader;
    ULONG Int1;
    ULONG Int2;
    ULONG Int3;
} MY_FILTER, *MY_FILTER;

MY_FILTER FilterData;
```

## -see-also

[ENABLE_TRACE_PARAMETERS](/windows/desktop/ETW/enable-trace-parameters)

[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)

[EnableTrace](/windows/desktop/ETW/enabletrace)

[EnableTraceEx](/windows/desktop/ETW/enabletraceex-func)

[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2)

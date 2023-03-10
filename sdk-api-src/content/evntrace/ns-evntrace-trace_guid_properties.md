---
UID: NS:evntrace._TRACE_GUID_PROPERTIES
title: TRACE_GUID_PROPERTIES (evntrace.h)
description:
  Returned by EnumerateTraceGuids. Contains information about an event trace
  provider.
helpviewer_keywords:
  [
    "*PTRACE_GUID_PROPERTIES",
    "PTRACE_GUID_PROPERTIES",
    "PTRACE_GUID_PROPERTIES structure pointer [ETW]",
    "TRACE_GUID_PROPERTIES",
    "TRACE_GUID_PROPERTIES structure [ETW]",
    "_TRACE_GUID_PROPERTIES",
    "_evt_trace_guid_properties",
    "base.trace_guid_properties",
    "etw.trace_guid_properties",
    "evntrace/PTRACE_GUID_PROPERTIES",
    "evntrace/TRACE_GUID_PROPERTIES",
  ]
old-location: etw\trace_guid_properties.htm
tech.root: ETW
ms.assetid: 849f2d34-14e0-43e8-a735-d46e94671725
ms.date: 12/05/2018
ms.keywords:
  "*PTRACE_GUID_PROPERTIES, PTRACE_GUID_PROPERTIES, PTRACE_GUID_PROPERTIES
  structure pointer [ETW], TRACE_GUID_PROPERTIES, TRACE_GUID_PROPERTIES
  structure [ETW], _TRACE_GUID_PROPERTIES, _evt_trace_guid_properties,
  base.trace_guid_properties, etw.trace_guid_properties,
  evntrace/PTRACE_GUID_PROPERTIES, evntrace/TRACE_GUID_PROPERTIES"
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TRACE_GUID_PROPERTIES, *PTRACE_GUID_PROPERTIES
req.redist:
ms.custom: 19H1
f1_keywords:
  - _TRACE_GUID_PROPERTIES
  - evntrace/_TRACE_GUID_PROPERTIES
  - PTRACE_GUID_PROPERTIES
  - evntrace/PTRACE_GUID_PROPERTIES
  - TRACE_GUID_PROPERTIES
  - evntrace/TRACE_GUID_PROPERTIES
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - Evntrace.h
api_name:
  - TRACE_GUID_PROPERTIES
---

# TRACE_GUID_PROPERTIES structure

## -description

Returned by
[EnumerateTraceGuids](/windows/win32/api/evntrace/nf-evntrace-enumeratetraceguids).
Contains information about an event trace provider.

## -struct-fields

### -field Guid

Control GUID of the event trace provider.

### -field GuidType

Not used.

### -field LoggerId

Session handle that identifies the event tracing session.

### -field EnableLevel

Value passed as the _EnableLevel_ parameter to the
[EnableTrace](/windows/desktop/ETW/enabletrace) function.

### -field EnableFlags

Value passed as the _EnableFlag_ parameter to the
[EnableTrace](/windows/desktop/ETW/enabletrace) function.

### -field IsEnable

If this member is **TRUE**, the element identified by the **Guid** member is
currently enabled for the session identified by the **LoggerId** member. If this
member is **FALSE**, all other members have no meaning and should be zero.

## -remarks

Be sure to initialize the memory for this structure to zero before setting any
members or passing to any functions.

## -see-also

[EnumerateTraceGuids](/windows/desktop/ETW/enumeratetraceguids)

---
UID: NS:evntrace._TRACE_GUID_REGISTRATION
title: TRACE_GUID_REGISTRATION (evntrace.h)
description: Used with RegisterTraceGuids to register event trace classes.
helpviewer_keywords:
  [
    "*PTRACE_GUID_REGISTRATION",
    "TRACE_GUID_REGISTRATION",
    "TRACE_GUID_REGISTRATION structure [ETW]",
    "_TRACE_GUID_REGISTRATION",
    "_evt_trace_guid_registration",
    "base.trace_guid_registration",
    "etw.trace_guid_registration",
    "evntrace/TRACE_GUID_REGISTRATION",
  ]
old-location: etw\trace_guid_registration.htm
tech.root: ETW
ms.assetid: fc7b61fb-ef1c-48ec-8523-5f3114b5407a
ms.date: 12/05/2018
ms.keywords:
  "*PTRACE_GUID_REGISTRATION, TRACE_GUID_REGISTRATION, TRACE_GUID_REGISTRATION
  structure [ETW], _TRACE_GUID_REGISTRATION, _evt_trace_guid_registration,
  base.trace_guid_registration, etw.trace_guid_registration,
  evntrace/TRACE_GUID_REGISTRATION"
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: TRACE_GUID_REGISTRATION, *PTRACE_GUID_REGISTRATION
req.redist:
ms.custom: 19H1
f1_keywords:
  - _TRACE_GUID_REGISTRATION
  - evntrace/_TRACE_GUID_REGISTRATION
  - PTRACE_GUID_REGISTRATION
  - evntrace/PTRACE_GUID_REGISTRATION
  - TRACE_GUID_REGISTRATION
  - evntrace/TRACE_GUID_REGISTRATION
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
  - TRACE_GUID_REGISTRATION
---

# TRACE_GUID_REGISTRATION structure

## -description

Used with
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)
to register event trace classes.

## -struct-fields

### -field Guid

Class GUID of an event trace class that you are registering.

### -field RegHandle

Handle to the registered event trace class. The
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)
function generates this value.

Use this handle when you call the
[CreateTraceInstanceId](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid)
function and to set the **RegHandle** member of
[EVENT_INSTANCE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_instance_header)
when calling the
[TraceEventInstance](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance)
function.

## -remarks

Be sure to initialize the memory for this structure to zero before setting any
members.

## -see-also

[CreateTraceInstanceId](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid)

[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)

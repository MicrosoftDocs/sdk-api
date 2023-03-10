---
UID: NF:evntrace.CreateTraceInstanceId
title: CreateTraceInstanceId function (evntrace.h)
description:
  A RegisterTraceGuids-based ("Classic") event provider uses the
  CreateTraceInstanceId function to create a unique transaction identifier and
  map it to a registration handle. The provider can then use the transaction
  identifier when calling the TraceEventInstance function.
helpviewer_keywords:
  [
    "CreateTraceInstanceId",
    "CreateTraceInstanceId function [ETW]",
    "_evt_createtraceinstanceid",
    "base.createtraceinstanceid",
    "etw.createtraceinstanceid",
    "evntrace/CreateTraceInstanceId",
  ]
old-location: etw\createtraceinstanceid.htm
tech.root: ETW
ms.assetid: ab890392-f1e4-4b4e-a46c-8c7c2bfd3897
ms.date: 12/05/2018
ms.keywords:
  CreateTraceInstanceId, CreateTraceInstanceId function [ETW],
  _evt_createtraceinstanceid, base.createtraceinstanceid,
  etw.createtraceinstanceid, evntrace/CreateTraceInstanceId
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - CreateTraceInstanceId
  - evntrace/CreateTraceInstanceId
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - Advapi32.dll
api_name:
  - CreateTraceInstanceId
---

# CreateTraceInstanceId function

## -description

A
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)-based
("Classic") event provider may use the **CreateTraceInstanceId** function to
create a unique transaction identifier and map it to a registration handle. The
provider then uses the transaction identifier when calling the
[TraceEventInstance](/windows/desktop/ETW/traceeventinstance) function to mark
events as belonging to the specified transaction. The transaction identifier can
be used by trace analysis tools to group events.

## -parameters

### -param RegHandle [in]

Handle to a registered event trace class. The
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)
function returns this handle in the **RegHandle** member of the
[TRACE_GUID_REGISTRATION](/windows/desktop/ETW/trace-guid-registration)
structure.

### -param InstInfo [out]

Pointer to an [EVENT_INSTANCE_INFO](/windows/desktop/ETW/event-instance-info)
structure. The **InstanceId** member of this structure contains the transaction
identifier.

## -returns

If the function is successful, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following are
some common errors and their causes.

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _RegHandle_ is **NULL**.
  - _pInstInfo_ is **NULL**.

## -remarks

RegisterTraceGuids-based ("Classic") providers call this function. Use
[EventActivityIdControl](/windows/win32/api/evntprov/nf-evntprov-eventactivityidcontrol)
for similar functionality with an EventRegister-based ("Crimson") provider.

ETW creates the identifier in the user-mode process, so it might return the same
number for different instances in different processes. The value starts over at
`1` when **InstanceId** reaches the maximum value for a **ULONG**. Only
user-mode providers can call the **CreateTraceInstanceId** function (drivers
cannot call this function).

### Examples

For an example that uses **CreateTraceInstanceId**, see
[Tracing Event Instances](/windows/desktop/ETW/tracing-event-instances).

## -see-also

[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)

[TraceEventInstance](/windows/desktop/ETW/traceeventinstance)

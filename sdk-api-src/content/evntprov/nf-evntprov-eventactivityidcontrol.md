---
UID: NF:evntprov.EventActivityIdControl
title: EventActivityIdControl function (evntprov.h)
description:
  Creates, queries, and sets activity identifiers for use in ETW events.
helpviewer_keywords:
  [
    "EVENT_ACTIVITY_CTRL_CREATE_ID",
    "EVENT_ACTIVITY_CTRL_CREATE_SET_ID",
    "EVENT_ACTIVITY_CTRL_GET_ID",
    "EVENT_ACTIVITY_CTRL_GET_SET_ID",
    "EVENT_ACTIVITY_CTRL_SET_ID",
    "EventActivityIdControl",
    "EventActivityIdControl function [ETW]",
    "base.eventactivityidcontrol_func",
    "etw.eventactivityidcontrol_func",
    "evntprov/EventActivityIdControl",
  ]
old-location: etw\eventactivityidcontrol_func.htm
tech.root: ETW
ms.assetid: 1c412909-bdff-4181-9750-f3444fda4c8f
ms.date: 12/05/2018
ms.keywords:
  EVENT_ACTIVITY_CTRL_CREATE_ID, EVENT_ACTIVITY_CTRL_CREATE_SET_ID,
  EVENT_ACTIVITY_CTRL_GET_ID, EVENT_ACTIVITY_CTRL_GET_SET_ID,
  EVENT_ACTIVITY_CTRL_SET_ID, EventActivityIdControl, EventActivityIdControl
  function [ETW], base.eventactivityidcontrol_func,
  etw.eventactivityidcontrol_func, evntprov/EventActivityIdControl
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
  - EventActivityIdControl
  - evntprov/EventActivityIdControl
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - Advapi32.dll
  - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
  - KernelBase.dll
  - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
  - API-MS-Win-eventing-provider-l1-1-0.dll
  - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
  - EventActivityIdControl
---

# EventActivityIdControl function

## -description

Creates, queries, and sets activity identifiers for use in ETW events.

## -parameters

### -param ControlCode [in]

A control code that specifies the operation to perform.

- **EVENT_ACTIVITY_CTRL_GET_ID**

  Sets the _ActivityId_ parameter to the value of the current thread's activity
  ID.

- **EVENT_ACTIVITY_CTRL_SET_ID**

  Sets the current thread's activity ID to the value of the _ActivityId_
  parameter.

- **EVENT_ACTIVITY_CTRL_CREATE_ID**

  Sets the _ActivityId_ parameter to the value of a newly-generated
  locally-unique activity ID.

- **EVENT_ACTIVITY_CTRL_GET_SET_ID**

  Swaps the values of the _ActivityId_ parameter and the current thread's
  activity ID. (Saves the value of the current thread's activity ID, then sets
  the current thread's activity ID to the value of the _ActivityId_ parameter,
  then sets the _ActivityId_ parameter to the saved value.)

- **EVENT_ACTIVITY_CTRL_CREATE_SET_ID**

  Sets the _ActivityId_ parameter to the value of the current thread's activity
  ID, then sets the current thread's activity ID to the value of a
  newly-generated locally-unique activity ID.

### -param ActivityId [in, out]

A pointer to a buffer that contains a 128-bit activity ID. This buffer may be
read-from and/or written-to, depending on the value of the _ControlCode_
parameter.

## -returns

Returns **ERROR_SUCCESS** if successful.

## -remarks

ETW events written using one of the **EventWrite** APIs will contain a 128-bit
"activity ID" field and can optionally contain a 128-bit "related activity ID"
field. Trace processing tools can use the values of these fields to organize
events into groups called activities.

- All events with an activity ID of zero (i.e. **GUID_NULL**) are assumed to not
  be a part of any activity.
- All events that have a particular non-zero activity ID are assumed to be a
  part of the same activity.
- To indicate the beginning of the activity, the provider should set Opcode to
  **WINEVENT_OPCODE_START** for the first event with a particular non-zero
  activity ID (the _start_ event). If the activity is logically nested within
  another activity, the provider should set the _start_ event's related activity
  ID field to the ID of the parent activity.
- To indicate the end of the activity, the provider should set Opcode to
  **WINEVENT_OPCODE_STOP** for the last event with a particular non-zero
  activity ID (the _stop_ event).

For activity IDs to be useful, newly-generated activity IDs must be
locally-unique, i.e. the same ID must not be generated twice within the trace.

You can create activity IDs using **EventActivityIdControl**, which generates
locally-unique IDs that are guaranteed to be unique across all processes on the
local system until the system reboots. You can also use a GUID (globally-unique
identifier) as an activity ID. You can create a GUID using an API such as
[UuidCreate](../rpcdce/nf-rpcdce-uuidcreate.md).

User-mode threads have a thread-local 128-bit activity ID value (the thread's
activity ID). The thread activity ID is initialized to 0 (i.e. **GUID_NULL**)
when the thread is created. The thread activity ID can be read or updated using
**EventActivityIdControl**. The thread activity ID will be used as the activity
ID for all events written by **EventWrite** and for all events written by
**EventWriteTransfer** or **EventWriteEx** where the _ActivityId_ parameter is
**NULL**.

> [!Important]
> A function that alters a thread's activity ID should be careful
> to restore the original activity ID before exiting. Otherwise, the function's
> changes to the thread's activity ID will interfere with the activities of
> components that call the function.

### Using an explicitly-specified activity ID

In cases where your activities are not limited to a single thread or where you
want to avoid the possibility of interference from other components overwriting
your thread's activity ID, you may want to explicitly specify event activities
via the _ActivityId_ field of **EventWriteTransfer** or **EventWriteEx** instead
of using the automatic thread activity ID.

If using [manifests](/windows/win32/etw/writing-manifest-based-events) and
[Message Compiler](/windows/win32/wes/message-compiler--mc-exe-) to write
events, the macros generated by `MC.exe -um` use the thread's activity ID while
the macros generated by `MC.exe -km` support an activity ID parameter.
Originally, the `-um` macros only worked in user-mode, and the `-km` macros only
worked in kernel-mode, so user-mode code could only use the current thread's
activity ID. However, starting with MC.exe version 10.0.17741, the macros
generated by `MC.exe -km` can be used for both user-mode and kernel-mode, so you
can use `MC.exe -km` to generate macros that accept an activity ID parameter.
(The MC-generated code does not support setting an event's related activity ID.)

If using [TraceLoggingProvider.h](/windows/win32/api/traceloggingprovider/) to
write events, the **TraceLoggingWrite** macro uses the thread's activity ID,
while the **TraceLoggingWriteActivity** accepts parameters for activity ID and
related activity ID. Alternatively, you can use the C++ classes in
[TraceLoggingActivity.h](/windows/win32/api/traceloggingactivity/) for your
TraceLogging activities.

## -see-also

[EventWriteTransfer](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer)

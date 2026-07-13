---
UID: NF:evntrace.ControlTraceW
title: ControlTraceW function (evntrace.h)
description: The ControlTraceW (Unicode) function (evntrace.h) flushes, queries, updates, or stops the specified event tracing session.
helpviewer_keywords:
  [
    "ControlTrace",
    "ControlTrace function [ETW]",
    "ControlTraceA",
    "ControlTraceW",
    "EVENT_TRACE_CONTROL_FLUSH",
    "EVENT_TRACE_CONTROL_QUERY",
    "EVENT_TRACE_CONTROL_STOP",
    "EVENT_TRACE_CONTROL_UPDATE",
    "_evt_controltrace",
    "base.controltrace",
    "etw.controltrace",
    "evntrace/ControlTrace",
    "evntrace/ControlTraceA",
    "evntrace/ControlTraceW",
  ]
old-location: etw\controltrace.htm
tech.root: ETW
ms.assetid: c39f669c-ff40-40ed-ba47-798474ec2de4
ms.date: 08/04/2022
ms.keywords:
  ControlTrace, ControlTrace function [ETW], ControlTraceA, ControlTraceW,
  EVENT_TRACE_CONTROL_FLUSH, EVENT_TRACE_CONTROL_QUERY,
  EVENT_TRACE_CONTROL_STOP, EVENT_TRACE_CONTROL_UPDATE, _evt_controltrace,
  base.controltrace, etw.controltrace, evntrace/ControlTrace,
  evntrace/ControlTraceA, evntrace/ControlTraceW
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: ControlTraceW (Unicode) and ControlTraceA (ANSI)
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib:
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012; Advapi32.dll on Windows 8,
  Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008,
  Windows Vista and Windows XP
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - ControlTraceW
  - evntrace/ControlTraceW
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-eventing-controller-l1-1-1.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - API-MS-Win-Eventing-Legacy-l1-1-0.dll
 - AdvApi32Legacy.dll
 - KernelBase.dll
api_name:
  - ControlTrace
  - ControlTraceA
  - ControlTraceW
---

# ControlTraceW function

## -description

The **ControlTrace** function flushes, queries, updates, or stops the specified
event tracing session.

## -parameters

### -param TraceHandle [in]

Handle to an event tracing session, or 0. You must specify a non-zero
_TraceHandle_ if _InstanceName_ is **NULL**. ETW ignores the handle if
_InstanceName_ is not **NULL**.

The [StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracew) function
returns this handle when a new trace is started. To obtain the handle of an
existing trace, use **ControlTrace** to query the trace properties based on the
trace's name and then get the handle from the **Wnode.HistoricalContext** field
of the returned `EVENT_TRACE_PROPERTIES` data.

### -param InstanceName [in]

Name of an event tracing session, or **NULL**. You must specify _InstanceName_
if _TraceHandle_ is 0.

To specify the NT Kernel Logger session, set _InstanceName_ to
**KERNEL_LOGGER_NAME**.

### -param Properties [in, out]

Pointer to an initialized
[EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
structure. This structure should be zeroed-out before setting any fields.

If _ControlCode_ specifies **EVENT_TRACE_CONTROL_STOP**,
**EVENT_TRACE_CONTROL_QUERY** or **EVENT_TRACE_CONTROL_FLUSH**, you only need to
set the **Wnode.BufferSize**, **Wnode.Guid**, **LoggerNameOffset**, and
**LogFileNameOffset** members of the
[EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
structure. If the session is a private session, you also need to set
**LogFileMode**. You can use the maximum session name (1024 characters) and
maximum log file name (1024 characters) lengths to calculate the buffer size and
offsets if not known.

If _ControlCode_ specifies **EVENT_TRACE_CONTROL_UPDATE**, on input, the members
must specify the new values for the properties to update. On output,
_Properties_ contains the properties and statistics for the event tracing
session. You can update the following properties.

- **EnableFlags**: Set this member to 0 to disable all system providers. Set
  this to a non-zero value to specify the system providers that you want to
  enable or keep enabled. This may be non-zero only for
  [system loggers](/windows/win32/api/evntrace/nf-evntrace-starttracew#system-loggers).

- **FlushTimer**: Set this member if you want to change the time to wait before
  flushing buffers. If this member is 0, the member is not updated.

- **LogFileNameOffset**: Set this member if you want to switch to another log
  file or to flush a buffering-mode trace to a new log file. If this member is
  0, the file name is not updated. If the offset is not zero and you do not
  change the log file name, the function returns an error.

- **LogFileMode**: Set this member if you want to turn
  **EVENT_TRACE_REAL_TIME_MODE** on and off. To turn real time consuming off,
  set this member to 0. To turn real time consuming on (creating a session that
  records to disk as well as delivering events in real-time), set this member to
  **EVENT_TRACE_REAL_TIME_MODE** and it will be OR'd with the current modes.

- **MaximumBuffers**: Set this member if you want to change the maximum number
  of buffers that ETW uses. If this member is 0, the member is not updated.

For private logger sessions, you can update only the **LogFileNameOffset** and
**FlushTimer** members.

If you are using a newly initialized
[EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
structure, zero-out the structure, then set **Wnode.BufferSize**,
**Wnode.Guid**, and **Wnode.Flags**, and the values you want to update.

If you are reusing a **EVENT_TRACE_PROPERTIES** structure (i.e. using a
structure that you previously passed to
[StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracew) or
**ControlTrace**), be sure to set the **LogFileNameOffset** member to 0 unless
you are changing the log file name, and be sure to set
[EVENT_TRACE_PROPERTIES.Wnode.Flags](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
to **WNODE_FLAG_TRACED_GUID**.

> **Starting with Windows 10, version 1703:** For better performance in cross
> process scenarios, you can now pass filtering information to **ControlTrace**
> for system wide private loggers. You will need to use the
> [EVENT_TRACE_PROPERTIES_V2](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
> structure to include filtering information. See
> [Configuring and Starting a Private Logger Session](/windows/win32/etw/configuring-and-starting-a-private-logger-session)
> for more details.

### -param ControlCode [in]

Requested control function. You can specify one of the following values:

- **EVENT_TRACE_CONTROL_FLUSH**: Flushes the session's active buffers.

  This can be used with an in-memory session (a session started with the
  **EVENT_TRACE_BUFFERING_MODE** flag) to write the data from the trace to a
  file.

  You do not normally need to flush file-based or real-time sessions because ETW
  will automatically flush a buffer when it is full (i.e. when it does not have
  room for the next event), when the trace session's FlushTimer expires, or when
  the trace session is closed.

  **Windows 2000:** This value is not supported.

- **EVENT_TRACE_CONTROL_QUERY**: Retrieves session properties and statistics.

- **EVENT_TRACE_CONTROL_STOP**: Stops the session. The session handle is no
  longer valid.

- **EVENT_TRACE_CONTROL_UPDATE**: Updates the session properties.

- **EVENT_TRACE_CONTROL_INCREMENT_FILE**: If the session has the
  `EVENT_TRACE_FILE_MODE_NEWFILE`, updates the session to switch to the next
  file immediately, rather than waiting for the prior file to fill up. Supported
  starting with Windows 10 October 2018 Update.

- **EVENT_TRACE_CONTROL_CONVERT_TO_REALTIME**: Changes a file mode session to a
  real-time session (enables real-time delivery and disables writing events to
  the ETL file). Supported starting with Windows 10 October 2020 Update.

> [!NOTE]
> It is not safe to flush buffers or stop a trace session from DllMain
> (may cause deadlock).

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_BAD_LENGTH**

  One of the following is true:

  - The **Wnode.BufferSize** member of _Properties_ specifies an incorrect size.
  - _Properties_ does not have sufficient space allocated to hold a copy of the
    session name and log file name (if used).

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _Properties_ is **NULL**.
  - _InstanceName_ and _TraceHandle_ are both **NULL**.
  - _InstanceName_ is **NULL** and _TraceHandle_ is not a valid handle.
  - The **LogFileNameOffset** member of _Properties_ is not valid.
  - The **LoggerNameOffset** member of _Properties_ is not valid.
  - The **LogFileMode** member of _Properties_ specifies a combination of flags
    that is not valid.
  - The **Wnode.Guid** member of _Properties_ is **SystemTraceControlGuid**, but
    the _InstanceName_ parameter is not `KERNEL_LOGGER_NAME`.

- **ERROR_BAD_PATHNAME**

  Another session is already using the file name specified by the
  **LogFileNameOffset** member of the _Properties_ structure.

- **ERROR_MORE_DATA**

  The buffer for
  [EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
  is too small to hold all the information for the session. If you do not need
  the session's property information, you can ignore this error. If you receive
  this error when stopping the session, ETW will have already stopped the
  session before generating this error.

- **ERROR_ACCESS_DENIED**

  Only users running with elevated administrative privileges, users in the
  Performance Log Users group, and services running as LocalSystem,
  LocalService, NetworkService can control event tracing sessions. To grant a
  restricted user the ability to control trace sessions, add them to the
  Performance Log Users group. Only users with administrative privileges and
  services running as LocalSystem can control an NT Kernel Logger session.

  **Windows XP and Windows 2000:** Anyone can control a trace session.

- **ERROR_WMI_INSTANCE_NOT_FOUND**

  The given session is not running.
  
- **ERROR_ACTIVE_CONNECTIONS**

  When returned from a EVENT_TRACE_CONTROL_STOP call, this indicates that
  the session is already in the process of stopping.

## -remarks

Event trace controllers call this function.

This function supersedes the
[FlushTrace](/windows/win32/api/evntrace/nf-evntrace-flushtracew),
[QueryTrace](/windows/win32/api/evntrace/nf-evntrace-querytracew),
[StopTrace](/windows/win32/api/evntrace/nf-evntrace-stoptracew), and
[UpdateTrace](/windows/win32/api/evntrace/nf-evntrace-updatetracew) functions.

> [!NOTE]
> The evntrace.h header defines ControlTrace as an alias which
> automatically selects the ANSI or Unicode version of this function based on
> the definition of the UNICODE preprocessor constant. Mixing usage of the
> encoding-neutral alias with code that not encoding-neutral can lead to
> mismatches that result in compilation or runtime errors. For more information,
> see
> [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

[QueryAllTraces](/windows/win32/api/evntrace/nf-evntrace-queryalltracesw)

[StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracew)

---
UID: NF:evntrace.StartTraceW
title: StartTraceW function (evntrace.h)
description: The StartTrace function starts an event tracing session. (Unicode)
helpviewer_keywords:
  [
    "StartTrace",
    "StartTrace function [ETW]",
    "StartTraceA",
    "StartTraceW",
    "_evt_starttrace",
    "base.starttrace",
    "etw.starttrace",
    "evntrace/StartTrace",
    "evntrace/StartTraceA",
    "evntrace/StartTraceW",
  ]
old-location: etw\starttrace.htm
tech.root: ETW
ms.assetid: c040514a-733d-44b9-8300-a8341d2630b3
ms.date: 12/05/2018
ms.keywords:
  StartTrace, StartTrace function [ETW], StartTraceA, StartTraceW,
  _evt_starttrace, base.starttrace, etw.starttrace, evntrace/StartTrace,
  evntrace/StartTraceA, evntrace/StartTraceW
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: StartTraceW (Unicode) and StartTraceA (ANSI)
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib:
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - StartTraceW
  - evntrace/StartTraceW
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
 - AdvApi32Legacy.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - API-MS-Win-Eventing-Legacy-l1-1-0.dll
 - KernelBase.dll
api_name:
  - StartTrace
  - StartTraceA
  - StartTraceW
---

# StartTraceW function

## -description

The **StartTrace** function registers and starts an event tracing session.

> [!Important]
> Cross-process event tracing sessions are a limited system
> resource. Developers should avoid starting event tracing sessions on customer
> machines. When event tracing sessions are needed, they should be limited to
> the smallest possible scope: use as few sessions as possible, use an
> in-process-only session if possible
> (`EVENT_TRACE_PRIVATE_LOGGER_MODE | EVENT_TRACE_PRIVATE_IN_PROC`), only start
> the trace when collection is specifically needed for a scenario, stop the
> trace as soon as the scenario is completed, limit the amount of memory used by
> the session, and use strict event filters so you do not collect unnecessary
> events.

## -parameters

### -param TraceHandle [out]

Receives the handle to the event tracing session for subsequent use with APIs
such as [ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew).

Do not use this handle if the function fails. Do not compare the session handle
to INVALID_HANDLE_VALUE. The session handle is 0 if the handle is not valid.

### -param InstanceName [in]

Null-terminated string that contains the name of the event tracing session. The
session name is limited to 1,024 characters, is case-insensitive, and must be
unique.

> [!Important]
> Use a descriptive name for your session so that the session's
> ownership and usage can be determined from the session name. Do not use a GUID
> or other non-deterministic or non-descriptive value. Do not append random
> digits to make your session name unique. ETW sessions are a limited resource
> so your component should not be starting multiple sessions. If your
> component's session is already running when your component starts, your
> component should clean up the orphaned session rather than creating a second
> session.

This function copies the session name that you provide to the offset that the
**LoggerNameOffset** member of _Properties_ points to.

### -param Properties [in, out]

Pointer to an
[EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
structure that specifies the behavior of the session. The following are key
members of the structure to set:

- **Wnode.BufferSize**
- **Wnode.Guid**
- **Wnode.ClientContext**
- **Wnode.Flags**
- **LogFileMode**
- **LogFileNameOffset**
- **LoggerNameOffset**

Depending on the type of log file you choose to create, you may also need to
specify a value for **MaximumFileSize**. See the Remarks section for more
information on setting the _Properties_ parameter and the behavior of the
session.

**Starting with Windows 10, version 1703:** For better performance in cross
process scenarios, you can now pass filtering in to **StartTrace** when starting
system wide private loggers. You will need to pass in the new
[EVENT_TRACE_PROPERTIES_V2](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
structure to include filtering information. See
[Configuring and Starting a Private Logger Session](/windows/win32/etw/configuring-and-starting-a-private-logger-session)
for more details.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_BAD_LENGTH**

  One of the following is true:

  - The **Wnode.BufferSize** member of _Properties_ specifies an incorrect size.
  - _Properties_ does not have sufficient space allocated to hold a copy of
    _InstanceName_.

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _Properties_ is **NULL**.
  - _TraceHandle_ is **NULL**.
  - The **LogFileNameOffset** member of _Properties_ is not valid.
  - The **LoggerNameOffset** member of _Properties_ is not valid.
  - The **LogFileMode** member of _Properties_ specifies a combination of flags
    that is not valid.
  - The **Wnode.Guid** member is **SystemTraceControlGuid**, but the
    _InstanceName_ parameter is not **KERNEL_LOGGER_NAME**.

- **ERROR_ALREADY_EXISTS**

  A session with the same name or GUID is already running.

- **ERROR_BAD_PATHNAME**

  You can receive this error for one of the following reasons:

  - Another session is already using the file name specified by the
    **LogFileNameOffset** member of the _Properties_ structure.
  - Both **LogFileMode** and **LogFileNameOffset** are zero.

- **ERROR_DISK_FULL**

  There is not enough free space on the drive for the log file. This occurs if:

  - **MaximumFileSize** is nonzero and there is not **MaximumFileSize** bytes
    available for the log file
  - the drive is a system drive and there is not an additional 200 MB available
  - **MaximumFileSize** is zero and there is not an additional 200 MB available

  Choose a drive with more space, or decrease the size specified in
  **MaximumFileSize** (if used).

- **ERROR_ACCESS_DENIED**

  Only users with administrative privileges, users in the Performance Log Users
  group, and services running as LocalSystem, LocalService, NetworkService can
  control event tracing sessions. To grant a restricted user the ability to
  control trace sessions, add them to the Performance Log Users group. Only
  users with administrative privileges and services running as LocalSystem can
  control an NT Kernel Logger session.

  If the user is a member of the Performance Log Users group, they may not have
  permission to create the log file in the specified folder.

- **ERROR_NO_SYSTEM_RESOURCES**

  One of the following is true:

  - The logging session uses the **EVENT_TRACE_SYSTEM_LOGGER_MODE** flag and the
    maximum number of system loggers (8) has been reached.

  - The maximum number of logging sessions on the system has been reached. No
    new loggers can be created until a logging session has been stopped. On most
    systems, the maximum number of logging sessions is 64.

    You can change the maximum number of logging sessions for a system by
    editing the **REG_DWORD** key at
    `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\WMI@EtwMaxLoggers`.
    Permissible values are 32 through 256, inclusive. A reboot is required for
    any change to take effect.

    Note that Loggers use system resources. Increasing the number of loggers on
    the system will come at a performance cost if those slots are filled. This
    limit exists to prevent excessive use of system resources.

    > [!Important]
    > The limit should only be manually adjusted by a system
    > administrator to enable specific scenarios. The EtwMaxLoggers setting must
    > not be automatically modified by a program or driver.

    Prior to Windows 10, version 1709, this is a fixed cap of 64 loggers for
    non-private loggers.

## -remarks

Event trace controllers call this function.

The session remains active until the session is stopped, the computer is
restarted, an I/O error occurs, or the maximum file size is reached for
non-circular logs. To stop an event tracing session, call the
[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew) function
and set the _ControlCode_ parameter to **EVENT_TRACE_CONTROL_STOP**.

You cannot start more than one session with the same session GUID (as specified
by `Properties.Wnode.Guid`). In most cases, you will set `Properties.Wnode.Guid`
to all-zero (i.e. **GUID_NULL**) to allow the ETW system to generate a new GUID
for the session.

To specify a private logger session, set **Wnode.Guid** member of _Properties_
to the provider's control GUID, not the private logger session's control GUID.
The provider must have registered the GUID before you call **StartTrace**.

You do not use this function to start a global logger session (deprecated). For
details on starting a global logger session, see
[Configuring and Starting the Global Logger Session](/windows/win32/etw/configuring-and-starting-the-global-logger-session).

### System Loggers

For the logger to be a system logger and receive events from
[SystemTraceProvider](/windows/desktop/ETW/configuring-and-starting-a-systemtraceprovider-session)
or other [system providers](/windows/win32/etw/system-providers), any of the
following must be true:

- The _Properties_ member **LogFileMode** includes the
  **EVENT_TRACE_SYSTEM_LOGGER_MODE** flag (preferred).
- The _Properties_ member **Wnode.Guid** is set to **SystemTraceControlGuid** or
  **GlobalLoggerGuid** (deprecated - should not be used for new code because it
  will conflict with other components that also try to use these GUIDs).
- _InstanceName_ is set to **KERNEL_LOGGER_NAME** (deprecated - should not be
  used for new code because it will conflict with other components that also try
  to use this name).

> [!NOTE]
> A system logger must set the **EnableFlags** member of the
> [EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
> structure to indicate which
> [SystemTraceProvider](/windows/win32/etw/configuring-and-starting-a-systemtraceprovider-session)
> events should be included in the trace.

Because system loggers receive special kernel events, they are subject to
additional restrictions:

- There can be no more than 8 system loggers active on the same system.
- System loggers cannot be created within a Windows Server container.
- System loggers cannot use the **EVENT_TRACE_USE_PAGED_MEMORY** flag.
- Prior to Windows 10, version 1703, no more than 2 distinct clock types can be
  used simultaneously by any system loggers. For example, if one active system
  logger is using the "CPU cycle counter" clock type, and another active system
  logger is using the "Query performance counter" clock type, then any attempt
  to start a system logger using the "System time" clock type will fail because
  it would require the activation of a third clock type. Because of this
  limitation, Microsoft strongly recommends that system loggers do not use the
  "System time" clock type.
- Starting with Windows 10, version 1703, the clock type restriction has been
  removed. All three clock types can now be used simultaneously by system
  loggers.

To specify an NT Kernel Logger session (deprecated), set _InstanceName_ to
**KERNEL_LOGGER_NAME** and the **Wnode.Guid** member of _Properties_ to
**SystemTraceControlGuid**. If you do not specify the GUID as
**SystemTraceControlGuid**, ETW will override the GUID value and set it to
**SystemTraceControlGuid**.

### Examples

For an example that uses **StartTrace**, see
[Configuring and Starting an Event Tracing Session](/windows/win32/etw/configuring-and-starting-an-event-tracing-session).

> [!NOTE]
> The evntrace.h header defines StartTrace as an alias which
> automatically selects the ANSI or Unicode version of this function based on
> the definition of the UNICODE preprocessor constant. Mixing usage of the
> encoding-neutral alias with code that not encoding-neutral can lead to
> mismatches that result in compilation or runtime errors. For more information,
> see
> [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew)

[EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

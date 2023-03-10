---
UID: NF:evntprov.EventRegister
title: EventRegister function (evntprov.h)
description:
  Registers an ETW event provider, creating a handle that can be used to write
  ETW events.
helpviewer_keywords:
  [
    "EventRegister",
    "EventRegister function [ETW]",
    "base.eventregister_func",
    "etw.eventregister_func",
    "evntprov/EventRegister",
  ]
old-location: etw\eventregister_func.htm
tech.root: ETW
ms.assetid: 6025c3a6-7d88-49dc-bbc3-655c172dde3c
ms.date: 12/05/2018
ms.keywords:
  EventRegister, EventRegister function [ETW], base.eventregister_func,
  etw.eventregister_func, evntprov/EventRegister
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
  - EventRegister
  - evntprov/EventRegister
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
  - bcrypt.dll
  - rtmpal.dll
api_name:
  - EventRegister
---

# EventRegister function

## -description

Registers an ETW event provider, creating a handle that can be used to write ETW
events.

## -parameters

### -param ProviderId [in]

GUID that uniquely identifies the provider, sometimes called a control GUID.
This must be a stable identifier so that trace controllers can use the GUID to
subscribe to events from this provider.

### -param EnableCallback [in, optional]

Optional
[EnableCallback](/windows/win32/api/evntprov/nc-evntprov-penablecallback) that
ETW will invoke when a trace session enables or disables this provider. Use
`NULL` if no callback is needed.

### -param CallbackContext [in, optional]

Optional context data that ETW will provide when invoking _EnableCallback_. Use
`NULL` if no callback context is needed.

### -param RegHandle [out]

Receives the event provider registration handle. The handle is used in
subsequent calls to provider APIs such as **EventWrite**,
**EventProviderEnabled**, and **EventRegister**.

Before your provider unloads or exits, free the provider registration handle by
calling
[EventUnregister](/windows/desktop/api/evntprov/nf-evntprov-eventunregister). A
DLL that unloads without freeing all of the provider handles that it registered
may cause the process to crash.

## -returns

Returns **ERROR_SUCCESS** if successful.

The error code returned by **EventRegister** is primarily intended for use in
debugging and diagnostic scenarios. Most production code should continue to run
even if an ETW provider failed to register, so release builds should usually
ignore the error code returned by **EventRegister**.

## -remarks

**EventRegister** creates a handle that you can use to write ETW events via
[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite),
[EventWriteTransfer](/windows/win32/api/evntprov/nf-evntprov-eventwritetransfer),
or [EventWriteEx](/windows/win32/api/evntprov/nf-evntprov-eventwriteex).

> [!Note]
> Most event providers will not call **EventRegister** directly.
> Instead, most event providers are implemented using an ETW framework that
> wraps the calls to **EventRegister**, **EventWrite**, and **EventUnregister**.
> For example, you might
> [write an event manifest](/windows/win32/etw/writing-manifest-based-events)
> and then use the
> [Message Compiler](/windows/win32/wes/message-compiler--mc-exe-) to generate
> C/C++ code for the events, or you might use
> [TraceLogging](/windows/win32/tracelogging/trace-logging-portal) to avoid the
> need for a manifest.

Registration of an event provider should not be confused with installation of an
event provider's manifest.

- The **EventRegister** API performs registration of an event provider to create
  a provider handle. This is a process-scope operation (the handle is valid only
  within the process). The handle can be used to write ETW events. All events
  written using the handle will be tagged with the _ProviderId_ that was
  specified during provider registration. It is not necessary to install a
  manifest to write events or capture traces (though installing the manifest may
  be necessary for decoding the provider's events or for the provider to work
  with Event Log).
- The [wevtutil.exe](/windows-server/administration/windows-commands/wevtutil)
  tool is used to install or uninstall an event provider's manifest.
  Installation of an event provider manifest means that information from the
  manifest is recorded on the system. The recorded information is system-global
  and persists until the manifest is uninstalled. The recorded information
  includes the names, GUIDs, channels, and resource DLL paths of the providers
  defined in the manifest. The information from the manifest is used by trace
  decoding tools and Event Log.

Most components will register their event provider at component initialization
and will unregister their event provider at component shutdown. For example, an
application (EXE) might register during application startup and unregister
during application exit. A dynamic library (DLL) might register in `DllMain`
during process attach and might unregister in `DllMain` during process detach.

Since event tracing is a debugging/diagnostic concern and is not normally
application-critical functionality, most retail applications should silently
ignore failures returned by **EventRegister**. In case of failure,
**EventRegister** will set the _RegHandle_ parameter to zero so that subsequent
uses of the RegHandle (i.e. in calls to **EventWrite** and **EventUnregister**)
will have no effect.

Each process can register up to 1,024 providers. However, you should limit the
number of providers that your component registers to one or two. This limit
includes providers registered using this function and providers registered using
[RegisterTraceGuids](/windows/desktop/ETW/registertraceguids).

**Prior to Windows Vista:** There is no specific limit to the number of
providers that a process can register.

## -see-also

[EnableCallback](/windows/desktop/api/evntprov/nc-evntprov-penablecallback)

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)

[EventUnregister](/windows/desktop/api/evntprov/nf-evntprov-eventunregister)

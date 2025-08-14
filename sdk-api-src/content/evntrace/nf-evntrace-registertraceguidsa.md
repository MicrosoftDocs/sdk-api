---
UID: NF:evntrace.RegisterTraceGuidsA
title: RegisterTraceGuidsA function (evntrace.h)
description: The RegisterTraceGuidsA (ANSI) function (evntrace.h) is an obsolete function, and new code should use the provided alternative.
helpviewer_keywords:
  [
    "RegisterTraceGuids",
    "RegisterTraceGuids function [ETW]",
    "RegisterTraceGuidsA",
    "RegisterTraceGuidsW",
    "_evt_registertraceguids",
    "base.registertraceguids",
    "etw.registertraceguids",
    "evntrace/RegisterTraceGuids",
    "evntrace/RegisterTraceGuidsA",
    "evntrace/RegisterTraceGuidsW",
  ]
old-location: etw\registertraceguids.htm
tech.root: ETW
ms.assetid: c9158292-281b-4a02-b280-956e340d225c
ms.date: 08/04/2022
ms.keywords:
  RegisterTraceGuids, RegisterTraceGuids function [ETW], RegisterTraceGuidsA,
  RegisterTraceGuidsW, _evt_registertraceguids, base.registertraceguids,
  etw.registertraceguids, evntrace/RegisterTraceGuids,
  evntrace/RegisterTraceGuidsA, evntrace/RegisterTraceGuidsW
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: RegisterTraceGuidsW (Unicode) and RegisterTraceGuidsA (ANSI)
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
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - RegisterTraceGuidsA
  - evntrace/RegisterTraceGuidsA
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-eventing-Obsolete-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
  - RegisterTraceGuids
  - RegisterTraceGuidsA
  - RegisterTraceGuidsW
---

# RegisterTraceGuidsA function

## -description

The **RegisterTraceGuids** function registers a
[Classic](/windows/win32/etw/tracing-events) (Windows 2000-style) ETW event
trace provider and the event trace classes that it uses to generate events. This
function also specifies the callback function the system uses to enable and
disable tracing from the provider.

This function is obsolete. New code should use
[EventRegister](/windows/win32/api/evntprov/nf-evntprov-eventregister) to
register a
[Windows Vista-style](/windows/win32/etw/writing-manifest-based-events)
(Crimson) ETW event trace provider.

## -parameters

### -param RequestAddress [in]

Pointer to a
[ControlCallback](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) function
that receives notification when the provider is enabled or disabled by an event
tracing session. The
[EnableTrace](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function
triggers this callback.

### -param RequestContext [in]

Pointer to an optional provider-defined context that ETW passes to the function
specified by _RequestAddress_.

### -param ControlGuid [in]

Control GUID (Provider ID) of the registering provider.

### -param GuidCount [in]

Number of elements in the _TraceGuidReg_ array. If _TraceGuidReg_ is **NULL**,
set this parameter to 0.

### -param TraceGuidReg [in, out]

Pointer to an array of  
[TRACE_GUID_REGISTRATION](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration)
structures.

Each element identifies a category of events that the provider provides.

On input, the **Guid** member of each structure contains an event trace class
GUID assigned by the registering provider. The class GUID identifies a category
of events that the provider provides. Providers use the same class GUID to set
the Guid member of
[EVENT_TRACE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)
when calling the
[TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log
the event.

On output, the **RegHandle** member receives a handle to the event's class GUID
registration. If the provider calls the
[TraceEventInstance](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance)
function, use the **RegHandle** member of
[TRACE_GUID_REGISTRATION](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration)
to set the **RegHandle** member of
[EVENT_INSTANCE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_instance_header).

This parameter can be **NULL** if the provider calls only the
[TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log
events. If the provider calls the
[TraceEventInstance](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance)
function to log events, this parameter cannot be **NULL**.

### -param MofImagePath [in]

This parameter is not supported. Set to **NULL**. You should use Mofcomp.exe to
register the MOF resource during the setup of your application. For more
information see,
[Publishing Your Event Schema](/windows/win32/etw/publishing-your-event-schema).

**Windows XP with SP1, Windows XP and Windows 2000:** Pointer to an optional
string that specifies the path of the DLL or executable program that contains
the resource specified by _MofResourceName_. This parameter can be **NULL** if
the event provider and consumer use another mechanism to share information about
the event trace classes used by the provider.

### -param MofResourceName [in]

This parameter is not supported. Set to **NULL**. You should use Mofcomp.exe to
register the MOF resource during the setup of your application. For more
information see,
[Publishing Your Event Schema](/windows/win32/etw/publishing-your-event-schema).

**Windows XP with SP1, Windows XP and Windows 2000:** Pointer to an optional
string that specifies the string resource of _MofImagePath_. The string resource
contains the name of the binary MOF file that describes the event trace classes
supported by the provider.

### -param RegistrationHandle [out]

Receives the provider's registration handle. Use the returned handle when you
call the
[UnregisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids)
function.

> [!Important]
> All registration handles created by a DLL or driver must be
> unregistered before the DLL or driver unloads. If the provider is not
> unregistered, a crash will occur when ETW tries to invoke the provider's
> callback.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following are
some common errors and their causes.

> [!Important]
> This function can also return the value returned by
> [ControlCallback](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) if a
> controller calls
> [EnableTrace](/windows/win32/api/evntrace/nf-evntrace-enabletrace) to enable
> the provider and the provider has not yet called **RegisterTraceGuids**. When
> this occurs, **RegisterTraceGuids** will return the return value of the
> callback if the registration was successful.

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _RequestAddress_ is **NULL**.
  - _ControlGuid_ is **NULL**.
  - _RegistrationHandle_ is **NULL**.

  **Windows XP and Windows 2000:** _TraceGuidReg_ is **NULL** or _GuidCount_ is
  less than or equal to zero.

## -remarks

> [!Note]
> Most developers will not call this function directly. Instead,
> developers will typically use an ETW framework. For example, TMF-based WPP
> manages the calls to **RegisterTraceGuids**, **TraceMessage**, and
> **UnregisterTraceGuids** on your behalf.

This function opens a [Classic](/windows/win32/etw/tracing-events) (Windows
2000-style) event provider handle that can be used to write MOF and TMF-based
WPP ETW events via
[TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent),
[TraceEventInstance](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance),
[TraceMessage](/windows/win32/api/evntrace/nf-evntrace-tracemessage), and
[TraceMessageVa](/windows/win32/api/evntrace/nf-evntrace-tracemessageva).

> [!Note]
> To open a
> [Windows Vista-style](/windows/win32/etw/writing-manifest-based-events)
> provider handle that writes manifest-based or TraceLogging-based ETW events
> via [EventWrite](/windows/win32/api/evntprov/nf-evntprov-eventwrite), use
> [EventRegister](/windows/win32/api/evntprov/nf-evntprov-eventregister).

If the provider's _ControlGuid_ has been previously registered and enabled,
subsequent registrations that reference the same _ControlGuid_ are automatically
enabled.

A process can register up to 1,024 provider GUIDs; however, you should limit the
number of providers that your process registers to one or two. This limit
includes those registered using this function and the
[EventRegister](/windows/win32/api/evntprov/nf-evntprov-eventregister) function.

**Prior to Windows Vista:** There is no limit to the number of providers that a
process can register.

### Examples

For an example that uses **RegisterTraceGuids**, see
[Writing Classic Events](/windows/win32/etw/tracing-events).

> [!NOTE]
> The evntrace.h header defines RegisterTraceGuids as an alias which
> automatically selects the ANSI or Unicode version of this function based on
> the definition of the UNICODE preprocessor constant. Mixing usage of the
> encoding-neutral alias with code that not encoding-neutral can lead to
> mismatches that result in compilation or runtime errors. For more information,
> see
> [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[EnableTrace](/windows/win32/api/evntrace/nf-evntrace-enabletrace)

[UnregisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids)

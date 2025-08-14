---
UID: NF:evntrace.SetTraceCallback
title: SetTraceCallback function (evntrace.h)
description:
  The SetTraceCallback function specifies an EventCallback function to process
  events for the specified event trace class. This function is obsolete.
helpviewer_keywords:
  [
    "SetTraceCallback",
    "SetTraceCallback function [ETW]",
    "_evt_settracecallback",
    "base.settracecallback",
    "etw.settracecallback",
    "evntrace/SetTraceCallback",
  ]
old-location: etw\settracecallback.htm
tech.root: ETW
ms.assetid: 8663f64f-a203-43e5-94e8-337f2d81c3a0
ms.date: 12/05/2018
ms.keywords:
  SetTraceCallback, SetTraceCallback function [ETW], _evt_settracecallback,
  base.settracecallback, etw.settracecallback, evntrace/SetTraceCallback
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
  - SetTraceCallback
  - evntrace/SetTraceCallback
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
 - KernelBase.dll
api_name:
  - SetTraceCallback
---

# SetTraceCallback function

## -description

> [!Important]
> Do not use this function; it may be unavailable in subsequent
> versions. Instead, filter for the event trace class in your
> [EventRecordCallback](/windows/desktop/ETW/eventrecordcallback) function.

The **SetTraceCallback** function specifies an
[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)
function to process events for the specified event trace class.

## -parameters

### -param pGuid [in]

Pointer to the class GUID of an event trace class for which you want to receive
events. For a list of kernel provider class GUIDs, see
[NT Kernel Logger Constants](/windows/desktop/ETW/nt-kernel-logger-constants).

### -param EventCallback [in]

Pointer to an
[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)
function used to process events belonging to the event trace class.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _pGuid_ is **NULL**.
  - _EventCallback_ is **NULL**.

## -remarks

Consumers call this function.

You can only specify one callback function for an event trace class. If you
specify more than one callback function for the event trace class, the last
callback function receives the events for that event trace class.

To stop the callback function from receiving events for the event trace class,
call the [RemoveTraceCallback](/windows/desktop/ETW/removetracecallback)
function. The callback automatically stops receiving callbacks when you close
the trace.

You can use this function to receive events written using one of the
[TraceEvent](/windows/desktop/ETW/traceevent) functions. You cannot use this
function to consume events from a provider that used one of the
[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite) functions to
log events.

## -see-also

[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)

[ProcessTrace](/windows/desktop/ETW/processtrace)

[RemoveTraceCallback](/windows/desktop/ETW/removetracecallback)

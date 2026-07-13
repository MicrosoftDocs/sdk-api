---
UID: NF:evntrace.CloseTrace
title: CloseTrace function (evntrace.h)
description:
  The CloseTrace function closes a trace processing session that was created
  with OpenTrace.
helpviewer_keywords:
  [
    "CloseTrace",
    "CloseTrace function [ETW]",
    "_evt_closetrace",
    "base.closetrace",
    "etw.closetrace",
    "evntrace/CloseTrace",
  ]
old-location: etw\closetrace.htm
tech.root: ETW
ms.assetid: 25f4c4d3-0b70-40fe-bf03-8f9ffd82fbec
ms.date: 12/05/2018
ms.keywords:
  CloseTrace, CloseTrace function [ETW], _evt_closetrace, base.closetrace,
  etw.closetrace, evntrace/CloseTrace
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
req.lib: AdvAPI32.Lib
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
  - CloseTrace
  - evntrace/CloseTrace
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-eventing-consumer-l1-1-2.dll
 - api-ms-win-eventing-consumer-l1-1-1.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Consumer-l1-1-0.dll
 - KernelBase.dll
api_name:
  - CloseTrace
---

# CloseTrace function

## -description

The **CloseTrace** function closes a trace processing session that was created
with [OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea).

## -parameters

### -param TraceHandle [in]

Handle to the trace processing session to close. The
[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea) function returns
this handle.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_INVALID_HANDLE**

  One of the following is true:

  - _TraceHandle_ is **0**.
  - _TraceHandle_ is **INVALID_PROCESSTRACE_HANDLE**.
  - _TraceHandle_ is not a valid handle.

- **ERROR_BUSY**

  Prior to Windows Vista, you cannot close the trace until the
  [ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace) function
  completes.

- **ERROR_CTX_CLOSE_PENDING**

  The call was successful. The
  [ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace) function
  will stop after it has processed all real-time events in its buffers (it will
  not receive any new events).

## -remarks

Consumers call this function to close a trace handle returned by **OpenTrace**.

> [!Important]
> Do not use this function to close the trace handle returned by
> **StartTrace**.

If you are processing events from a log file, you call this function only after
the [ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace)
function returns. However, if you are processing real-time events, you can call
this function before **ProcessTrace** returns. (Another way to stop trace
processing is to return FALSE from
[BufferCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka).)

If you call this function before **ProcessTrace** returns, the **CloseTrace**
function returns ERROR_CTX_CLOSE_PENDING. The ERROR_CTX_CLOSE_PENDING code
indicates that the **CloseTrace** function call was successful; the
**ProcessTrace** function will stop processing events after it processes all
previously-queued events (**ProcessTrace** will not receive any new events after
you call the **CloseTrace** function). You can call the **CloseTrace** function
from your [BufferCallback](/windows/desktop/ETW/buffercallback),
[EventCallback](/windows/desktop/ETW/eventcallback), or
[EventClassCallback](/windows/desktop/ETW/eventclasscallback) callback.

> **Prior to Windows Vista:** You can call **CloseTrace** only after
> [ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace) returns.

### Examples

For an example that uses **CloseTrace**, see
[Retrieving Event Data Using TDH](/windows/desktop/ETW/retrieving-event-data-using-tdh).

## -see-also

[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea)

[ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace)

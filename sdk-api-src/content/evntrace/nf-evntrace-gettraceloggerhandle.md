---
UID: NF:evntrace.GetTraceLoggerHandle
title: GetTraceLoggerHandle function (evntrace.h)
description:
  A RegisterTraceGuids-based ("Classic") event provider uses the
  GetTraceLoggerHandle function to retrieve the handle of the event tracing
  session to which it should write events. Providers call this function from
  their ControlCallback function.
helpviewer_keywords:
  [
    "GetTraceLoggerHandle",
    "GetTraceLoggerHandle function [ETW]",
    "_evt_gettraceloggerhandle",
    "base.gettraceloggerhandle",
    "etw.gettraceloggerhandle",
    "evntrace/GetTraceLoggerHandle",
  ]
old-location: etw\gettraceloggerhandle.htm
tech.root: ETW
ms.assetid: 050d3a01-0087-40f1-af35-b9ceeaf47813
ms.date: 12/05/2018
ms.keywords:
  GetTraceLoggerHandle, GetTraceLoggerHandle function [ETW],
  _evt_gettraceloggerhandle, base.gettraceloggerhandle,
  etw.gettraceloggerhandle, evntrace/GetTraceLoggerHandle
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - GetTraceLoggerHandle
  - evntrace/GetTraceLoggerHandle
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
  - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
  - GetTraceLoggerHandle
---

# GetTraceLoggerHandle function

## -description

A
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)-based
("Classic") event provider uses the **GetTraceLoggerHandle** function to
retrieve the handle of the event tracing session to which it should write
events.

Providers call this function from their
[ControlCallback](/windows/desktop/ETW/controlcallback) function.

## -parameters

### -param Buffer [in]

Pointer to a [WNODE_HEADER](/windows/desktop/ETW/wnode-header) structure. ETW
passes this structure to the provider's
[ControlCallback](/windows/desktop/ETW/controlcallback) function in the _Buffer_
parameter.

The **HistoricalContext** member of
[WNODE_HEADER](/windows/desktop/ETW/wnode-header) contains the session's handle.

## -returns

If the function succeeds, it returns the event tracing session handle.

If the function fails, it returns **INVALID_HANDLE_VALUE**. To get extended
error information, call the
[GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
function.

## -remarks

You use the handle when calling the
[GetTraceEnableFlags](/windows/desktop/ETW/gettraceenableflags) and
[GetTraceEnableLevel](/windows/desktop/ETW/gettraceenablelevel) functions to
retrieve the enable flags and level values passed to the
[EnableTrace](/windows/desktop/ETW/enabletrace) function.

### Examples

For an example that uses **GetTraceLoggerHandle**, see
[Retrieving Event Data Using MOF](/windows/desktop/ETW/retrieving-event-data-using-mof).

## -see-also

[GetTraceEnableFlags](/windows/desktop/ETW/gettraceenableflags)

[GetTraceEnableLevel](/windows/desktop/ETW/gettraceenablelevel)

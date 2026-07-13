---
UID: NF:evntrace.TraceQueryInformation
title: TraceQueryInformation function (evntrace.h)
description: Provides information about an event tracing session.
helpviewer_keywords:
  [
    "TraceQueryInformation",
    "TraceQueryInformation function [ETW]",
    "etw.tracequeryinformation",
    "evntrace/TraceQueryInformation",
  ]
old-location: etw\tracequeryinformation.htm
tech.root: ETW
ms.assetid: 3CC91F7C-7F82-4B3B-AA50-FE03CFEC0278
ms.date: 12/05/2018
ms.keywords:
  TraceQueryInformation, TraceQueryInformation function [ETW],
  etw.tracequeryinformation, evntrace/TraceQueryInformation
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
  Windows 8 and Windows Server 2012
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8 and Windows Server 2012
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - TraceQueryInformation
  - evntrace/TraceQueryInformation
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-eventing-controller-l1-1-1.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - KernelBase.dll
api_name:
  - TraceQueryInformation
---

# TraceQueryInformation function

## -description

The **TraceQueryInformation** function provides information about an event
tracing session.

## -parameters

### -param SessionHandle [in]

Handle of the event tracing session for which you are collecting information.
The [StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracea) function
returns this handle when a new trace is started. To obtain the handle of an
existing trace, use
[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew) to query
the trace properties based on the trace's name and then get the handle from the
**Wnode.HistoricalContext** field of the returned `EVENT_TRACE_PROPERTIES` data.

### -param InformationClass [in]

The information class to query. The information that the class captures is
included in the extended data section of the event. For a list of information
classes that you can query, see the
[TRACE_QUERY_INFO_CLASS](/windows/desktop/ETW/trace-info-class) enumeration.

### -param TraceInformation [out]

A pointer to a buffer to receive the returned information class specific data.
The information class determines the contents of this parameter. For example,
for the **TraceStackTracingInfo** information class, this parameter is an array
of [CLASSIC_EVENT_ID](/windows/desktop/ETW/classic-event-id) structures. The
structures specify the event GUIDs for which stack tracing is enabled. The array
is limited to 256 elements.

### -param InformationLength [in]

The size, in bytes, of the data returned in the _TraceInformation_ buffer. If
the function fails, this value indicates the required size of the
_TraceInformation_ buffer that is needed.

### -param ReturnLength [out, optional]

A pointer a value that receives the size, in bytes, of the specific data
returned in the _TraceInformation_ buffer.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the following error codes.

- **ERROR_BAD_LENGTH**

  The program issued a command but the command length is incorrect. This error
  is returned if the _InformationLength_ parameter is less than a minimum size.

- **ERROR_INVALID_PARAMETER**

  The parameter is incorrect.

- **ERROR_NOT_SUPPORTED**

  The request is not supported.

- **Other**

  Use [FormatMessage](/windows/desktop/api/winbase/nf-winbase-formatmessage) to
  obtain the message string for the returned error.

## -remarks

The **TraceQueryInformation** function queries event tracing session settings
from a trace session. Call this function after calling
[StartTrace](/windows/desktop/ETW/starttrace).

## -see-also

[TRACE_QUERY_INFO_CLASS](/windows/desktop/ETW/trace-info-class)

[TraceSetInformation](/windows/desktop/ETW/tracesetinformation)

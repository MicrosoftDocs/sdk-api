---
UID: NF:evntrace.TraceSetInformation
title: TraceSetInformation function (evntrace.h)
description: Configures event tracing session settings.
helpviewer_keywords:
  [
    "TraceSetInformation",
    "TraceSetInformation function [ETW]",
    "etw.tracesetinformation",
    "evntrace/TraceSetInformation",
  ]
old-location: etw\tracesetinformation.htm
tech.root: ETW
ms.assetid: f4cdbe32-6885-4844-add5-560961c3dd1d
ms.date: 12/05/2018
ms.keywords:
  TraceSetInformation, TraceSetInformation function [ETW],
  etw.tracesetinformation, evntrace/TraceSetInformation
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
  Windows 8, Windows Server 2012, Windows 7 and Windows Server 2008 R2
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7 and Windows Server 2008 R2
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - TraceSetInformation
  - evntrace/TraceSetInformation
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
 - KernelBase.dll
api_name:
  - TraceSetInformation
---

# TraceSetInformation function

## -description

The **TraceSetInformation** function configures event tracing session settings.

## -parameters

### -param SessionHandle [in]

Handle of the event tracing session to be configured. The
[StartTrace](/windows/win32/api/evntrace/nf-evntrace-starttracea) function
returns this handle when a new trace is started. To obtain the handle of an
existing trace, use
[ControlTrace](/windows/win32/api/evntrace/nf-evntrace-controltracew) to query
the trace properties based on the trace's name and then get the handle from the
**Wnode.HistoricalContext** field of the returned `EVENT_TRACE_PROPERTIES` data.

### -param InformationClass [in]

The information class to enable or disable. The information that the class
captures is included in the extended data section of the event. For a list of
information classes that you can enable, see the
[TRACE_QUERY_INFO_CLASS](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)
enumeration.

### -param TraceInformation [in]

A pointer to information class specific data. The information class determines
the contents of this parameter.

### -param InformationLength [in]

The size, in bytes, of the data in the _TraceInformation_ buffer.

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

Call this function after calling [StartTrace](/windows/desktop/ETW/starttrace).

If the _InformationClass_ parameter is set to **TraceStackTracingInfo**, calling
this function enables stack tracing of the specified kernel events. Subsequent
calls to this function overwrites the previous list of kernel events for which
stack tracing is enabled. To disable stack tracing, call this function with
_InformationClass_ set to **TraceStackTracingInfo** and _InformationLength_ set
to 0.

The extended data section of the event will include the call stack. The
[StackWalk_Event](/windows/desktop/ETW/stackwalk-event) MOF class defines the
layout of the extended data.

Typically, on 64-bit computers, you cannot capture the kernel stack in certain
contexts when page faults are not allowed. To enable walking the kernel stack on
x64, set the `DisablePagingExecutive` Memory Management registry value to 1. The
`DisablePagingExecutive` registry value is located under the following registry
key:
`HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management`.
This should only be done for temporary diagnosis purposes because it increases
memory usage of the system.

## -see-also

[TRACE_QUERY_INFO_CLASS](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

[TraceQueryInformation](/windows/desktop/ETW/tracequeryinformation)

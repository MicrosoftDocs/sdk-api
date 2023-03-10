---
UID: NS:evntrace._TRACE_VERSION_INFO
title: TRACE_VERSION_INFO (evntrace.h)
description: Determines the version information of the TraceLogging session.
helpviewer_keywords:
  [
    "*PTRACE_VERSION_INFO",
    "PTRACE_VERSION_INFO",
    "PTRACE_VERSION_INFO structure pointer [ETW]",
    "TRACE_VERSION_INFO",
    "TRACE_VERSION_INFO structure [ETW]",
    "etw.trace_version_info",
    "evntrace/PTRACE_VERSION_INFO",
    "evntrace/TRACE_VERSION_INFO",
  ]
old-location: etw\trace_version_info.htm
tech.root: ETW
ms.assetid: E2B291DB-928F-4170-8684-4B26A7E067BD
ms.date: 12/05/2018
ms.keywords:
  "*PTRACE_VERSION_INFO, PTRACE_VERSION_INFO, PTRACE_VERSION_INFO structure
  pointer [ETW], TRACE_VERSION_INFO, TRACE_VERSION_INFO structure [ETW],
  etw.trace_version_info, evntrace/PTRACE_VERSION_INFO,
  evntrace/TRACE_VERSION_INFO"
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.dll:
req.irql:
targetos: Windows
req.typenames: TRACE_VERSION_INFO, *PTRACE_VERSION_INFO
req.redist:
ms.custom: 19H1
f1_keywords:
  - _TRACE_VERSION_INFO
  - evntrace/_TRACE_VERSION_INFO
  - PTRACE_VERSION_INFO
  - evntrace/PTRACE_VERSION_INFO
  - TRACE_VERSION_INFO
  - evntrace/TRACE_VERSION_INFO
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - Evntrace.h
api_name:
  - TRACE_VERSION_INFO
---

# TRACE_VERSION_INFO structure

## -description

Determines the version information of the trace processing API.
This data is returned from
[TraceQueryInformation](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)
when called with the
[TraceVersionInfo](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)
information class.

## -struct-fields

### -field EtwTraceProcessingVersion

The version of the trace processing API on the current system.

### -field Reserved

Not used.

## -see-also

[TraceQueryInformation](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

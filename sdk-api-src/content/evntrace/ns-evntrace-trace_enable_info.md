---
UID: NS:evntrace._TRACE_ENABLE_INFO
title: TRACE_ENABLE_INFO (evntrace.h)
description:
  Defines the session and the information that the session used to enable the
  provider.
helpviewer_keywords:
  [
    "*PTRACE_ENABLE_INFO",
    "PTRACE_ENABLE_INFO",
    "PTRACE_ENABLE_INFO structure pointer [ETW]",
    "TRACE_ENABLE_INFO",
    "TRACE_ENABLE_INFO structure [ETW]",
    "_TRACE_ENABLE_INFO",
    "etw.trace_enable_info",
    "evntrace/PTRACE_ENABLE_INFO",
    "evntrace/TRACE_ENABLE_INFO",
  ]
old-location: etw\trace_enable_info.htm
tech.root: ETW
ms.assetid: 999dd102-5937-4b1e-b841-623dddaa0df9
ms.date: 12/05/2018
ms.keywords:
  "*PTRACE_ENABLE_INFO, PTRACE_ENABLE_INFO, PTRACE_ENABLE_INFO structure pointer
  [ETW], TRACE_ENABLE_INFO, TRACE_ENABLE_INFO structure [ETW],
  _TRACE_ENABLE_INFO, etw.trace_enable_info, evntrace/PTRACE_ENABLE_INFO,
  evntrace/TRACE_ENABLE_INFO"
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt:
req.target-min-winversvr:
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
req.typenames: TRACE_ENABLE_INFO, *PTRACE_ENABLE_INFO
req.redist:
ms.custom: 19H1
f1_keywords:
  - _TRACE_ENABLE_INFO
  - evntrace/_TRACE_ENABLE_INFO
  - PTRACE_ENABLE_INFO
  - evntrace/PTRACE_ENABLE_INFO
  - TRACE_ENABLE_INFO
  - evntrace/TRACE_ENABLE_INFO
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
  - TRACE_ENABLE_INFO
---

# TRACE_ENABLE_INFO structure

## -description

Defines the session and the information that the session used to enable the
provider. This information is returned by
[EnumerateTraceGuidsEx](/windows/win32/api/evntrace/nf-evntrace-enumeratetraceguidsex)
as part of a
[TRACE_PROVIDER_INSTANCE_INFO](/windows/win32/api/evntrace/ns-evntrace-trace_provider_instance_info)
block.

## -struct-fields

### -field IsEnabled

Indicates if the provider is enabled to the session. The value is **TRUE** if
the provider is enabled to the session, otherwise, the value is **FALSE**. This
value should always be **TRUE**.

### -field Level

Level of detail that the session asked the provider to include in the events.
For details, see the _Level_ parameter of the
[EnableTraceEx](/windows/desktop/ETW/enabletraceex-func) function.

### -field Reserved1

Reserved.

### -field LoggerId

Identifies the session that enabled the provider.

### -field EnableProperty

Additional information that the session wants ETW to include in the log file.
For details, see the _EnableProperty_ parameter of the
[EnableTraceEx](/windows/desktop/ETW/enabletraceex-func) function.

### -field Reserved2

Reserved.

### -field MatchAnyKeyword

Keywords specify which events the session wants the provider to write. For
details, see the _MatchAnyKeyword_ parameter of the
[EnableTraceEx](/windows/desktop/ETW/enabletraceex-func) function.

### -field MatchAllKeyword

Keywords specify which events the session wants the provider to write. For
details, see the _MatchAllKeyword_ parameter of the
[EnableTraceEx](/windows/desktop/ETW/enabletraceex-func) function.

## -remarks

The
[TRACE_PROVIDER_INSTANCE_INFO](/windows/win32/api/evntrace/ns-evntrace-trace_provider_instance_info)
block contains one or more of these structures.

## -see-also

[TRACE_PROVIDER_INSTANCE_INFO](/windows/win32/api/evntrace/ns-evntrace-trace_provider_instance_info)

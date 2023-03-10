---
UID: NS:evntrace._TRACE_PROVIDER_INSTANCE_INFO
title: TRACE_PROVIDER_INSTANCE_INFO (evntrace.h)
description: Defines an instance of the provider GUID.
helpviewer_keywords:
  [
    "*PTRACE_PROVIDER_INSTANCE_INFO",
    "PTRACE_PROVIDER_INSTANCE_INFO",
    "PTRACE_PROVIDER_INSTANCE_INFO structure pointer [ETW]",
    "TRACE_PROVIDER_FLAG_LEGACY",
    "TRACE_PROVIDER_FLAG_PRE_ENABLE",
    "TRACE_PROVIDER_INSTANCE_INFO",
    "TRACE_PROVIDER_INSTANCE_INFO structure [ETW]",
    "_TRACE_PROVIDER_INSTANCE_INFO",
    "etw.trace_provider_instance_info",
    "evntrace/PTRACE_PROVIDER_INSTANCE_INFO",
    "evntrace/TRACE_PROVIDER_INSTANCE_INFO",
  ]
old-location: etw\trace_provider_instance_info.htm
tech.root: ETW
ms.assetid: 49c11cd5-2cb1-474a-8b51-2d86b4501da1
ms.date: 12/05/2018
ms.keywords:
  "*PTRACE_PROVIDER_INSTANCE_INFO, PTRACE_PROVIDER_INSTANCE_INFO,
  PTRACE_PROVIDER_INSTANCE_INFO structure pointer [ETW],
  TRACE_PROVIDER_FLAG_LEGACY, TRACE_PROVIDER_FLAG_PRE_ENABLE,
  TRACE_PROVIDER_INSTANCE_INFO, TRACE_PROVIDER_INSTANCE_INFO structure [ETW],
  _TRACE_PROVIDER_INSTANCE_INFO, etw.trace_provider_instance_info,
  evntrace/PTRACE_PROVIDER_INSTANCE_INFO, evntrace/TRACE_PROVIDER_INSTANCE_INFO"
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
req.typenames: TRACE_PROVIDER_INSTANCE_INFO, *PTRACE_PROVIDER_INSTANCE_INFO
req.redist:
ms.custom: 19H1
f1_keywords:
  - _TRACE_PROVIDER_INSTANCE_INFO
  - evntrace/_TRACE_PROVIDER_INSTANCE_INFO
  - PTRACE_PROVIDER_INSTANCE_INFO
  - evntrace/PTRACE_PROVIDER_INSTANCE_INFO
  - TRACE_PROVIDER_INSTANCE_INFO
  - evntrace/TRACE_PROVIDER_INSTANCE_INFO
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
  - TRACE_PROVIDER_INSTANCE_INFO
---

# TRACE_PROVIDER_INSTANCE_INFO structure

## -description

Defines an instance of the provider GUID. This data is returned from
[EnumerateTraceGuidsEx](/windows/win32/api/evntrace/nf-evntrace-enumeratetraceguidsex)
when called with the
[TraceGuidQueryInfo](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)
information class.

## -struct-fields

### -field NextOffset

Offset, in bytes, from the beginning of this structure to the next
**TRACE_PROVIDER_INSTANCE_INFO** structure. The value is zero if there is not
another instance info block.

### -field EnableCount

Number of [TRACE_ENABLE_INFO](/windows/desktop/ETW/trace-enable-info) structures
in this block. Each structure represents a session that enabled the provider.

### -field Pid

Process identifier of the process that registered the provider.

### -field Flags

Can be one of the following flags.

- **TRACE_PROVIDER_FLAG_LEGACY**: The provider used
  [RegisterTraceGuids](/windows/desktop/ETW/registertraceguids) instead of
  [EventRegister](/windows/desktop/api/evntprov/nf-evntprov-eventregister) to
  register itself.

- **TRACE_PROVIDER_FLAG_PRE_ENABLE**: The provider is not registered; however,
  one or more sessions have enabled the provider.

## -remarks

If more than one event provider has registered using the same provider GUID, the
[TRACE_GUID_INFO](/windows/desktop/ETW/trace-guid-info) block contains more than
one **TRACE_PROVIDER_INSTANCE_INFO** structure.

## -see-also

[TRACE_ENABLE_INFO](/windows/desktop/ETW/trace-enable-info)

[TRACE_GUID_INFO](/windows/desktop/ETW/trace-guid-info)

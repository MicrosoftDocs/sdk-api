---
UID: NS:evntrace.TRACE_CONTEXT_REGISTER_INFO
tech.root: ETW
title: TRACE_CONTEXT_REGISTER_INFO
ms.date: 06/06/2024
targetos: Windows
description: Identifies the set of registers to be logged when enabling Context Register Tracing.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: evntrace.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: Windows Server 23H2
req.target-type: 
req.typenames: TRACE_CONTEXT_REGISTER_INFO
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntrace.h
api_name:
 - TRACE_CONTEXT_REGISTER_INFO
f1_keywords:
 - TRACE_CONTEXT_REGISTER_INFO
 - evntrace/TRACE_CONTEXT_REGISTER_INFO
dev_langs:
 - c++
helpviewer_keywords: ["TRACE_CONTEXT_REGISTER_INFO", "TRACE_CONTEXT_REGISTER_INFO structure [ETW]", "etw.etw_context_register_info", "evntrace/TRACE_CONTEXT_REGISTER_INFO"]
---

## -description

Identifies the set of registers to be logged when enabling Context Register Tracing. Used when the
[TraceContextRegisterInfo](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) value is specified as the *InformationClass* parameter of the [TraceSetInformation](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function.

## -struct-fields

### -field RegisterTypes

This field specifies which CPU registers should be logged when triggered by a
related system event. Multiple flag values can be combined using bit-wise OR.
For supported values, see [ETW_CONTEXT_REGISTER_TYPES](ne-evntrace-etw_context_register_types.md).

### -field Reserved

Reserved.

## -remarks

Currently, both [EtwContextRegisterTypeControl](ne-evntrace-etw_context_register_types.md) and [EtwContextRegisterTypeInteger](ne-evntrace-etw_context_register_types.md) must be set for correct operation of this API.

## -see-also


---
UID: NE:evntrace.ETW_CONTEXT_REGISTER_TYPES
tech.root: ETW
title: ETW_CONTEXT_REGISTER_TYPES
ms.date: 06/06/2024
targetos: Windows
description: Specifies the set of registers to be collected when Context Register Tracing is enabled.
prerelease: true
req.construct-type: enumeration
req.ddi-compliance: 
req.header: evntrace.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: Windows Server 23H2
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntrace.h
api_name:
 - ETW_CONTEXT_REGISTER_TYPES
f1_keywords:
 - ETW_CONTEXT_REGISTER_TYPES
 - evntrace/ETW_CONTEXT_REGISTER_TYPES
dev_langs:
 - c++
helpviewer_keywords:
 - ETW_CONTEXT_REGISTER_TYPES
---

## -description

Specifies the set of CPU registers to be collected when Context Register Tracing is enabled. This enumeration is used by the [TRACE_CONTEXT_REGISTER_INFO](ns-evntrace-trace_context_register_info.md)
structure.

## -enum-fields

### -field EtwContextRegisterTypeNone

No register types.

### -field EtwContextRegisterTypeControl

Control register types. The exact registers vary by architecture.

### -field EtwContextRegisterTypeInteger

Integer register types. The exact registers vary by architecture.

## -remarks

On AMD64, the integer registers include Rax, Rbx, Rcx, Rsi, Rbp, R8, and others. On AMD64, the control registers include Rip, SegCs, SegSs, Rsp, and EFlags. For more information on supported registers, see [CONTEXT structure](/windows/win32/api/winnt/ns-winnt-context).

## -see-also


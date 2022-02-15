---
UID: NS:evntrace._MOF_FIELD
title: MOF_FIELD (evntrace.h)
description:
  You may use the MOF_FIELD structures to append event data to the
  EVENT_TRACE_HEADER or EVENT_INSTANCE_HEADER structures.
helpviewer_keywords:
  [
    "*PMOF_FIELD",
    "MOF_FIELD",
    "MOF_FIELD structure [ETW]",
    "PMOF_FIELD",
    "PMOF_FIELD structure pointer [ETW]",
    "_MOF_FIELD",
    "_evt_mof_field",
    "base.mof_field",
    "etw.mof_field",
    "evntrace/MOF_FIELD",
    "evntrace/PMOF_FIELD",
  ]
old-location: etw\mof_field.htm
tech.root: ETW
ms.assetid: 64ff1191-2177-4d51-afcd-b58d510e9ae8
ms.date: 12/05/2018
ms.keywords:
  "*PMOF_FIELD, MOF_FIELD, MOF_FIELD structure [ETW], PMOF_FIELD, PMOF_FIELD
  structure pointer [ETW], _MOF_FIELD, _evt_mof_field, base.mof_field,
  etw.mof_field, evntrace/MOF_FIELD, evntrace/PMOF_FIELD"
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
req.dll:
req.irql:
targetos: Windows
req.typenames: MOF_FIELD, *PMOF_FIELD
req.redist:
ms.custom: 19H1
f1_keywords:
  - _MOF_FIELD
  - evntrace/_MOF_FIELD
  - PMOF_FIELD
  - evntrace/PMOF_FIELD
  - MOF_FIELD
  - evntrace/MOF_FIELD
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
  - MOF_FIELD
---

# MOF_FIELD structure

## -description

You may use the **MOF_FIELD** structures to append event data to the
[EVENT_TRACE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)
or
[EVENT_INSTANCE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_instance_header)
structures.

## -struct-fields

### -field DataPtr

Pointer to a event data item.

### -field Length

Length of the item pointed to by **DataPtr**, in bytes.

### -field DataType

Reserved.

## -remarks

Be sure to initialize the memory for this structure to zero before setting any
members.

If you use **MOF_FIELD** structures, you must set the **WNODE_FLAG_USE_MOF_PTR**
flag in the **Flags** member of the
[EVENT_TRACE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)
or
[EVENT_INSTANCE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_instance_header)
structures.

The event tracing session automatically dereferences **MOF_FIELD** data pointers
before passing the data to event trace consumers using
[EVENT_TRACE](/windows/win32/api/evntrace/ns-evntrace-event_trace) structures.

## -see-also

[EVENT_INSTANCE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_instance_header)

[EVENT_TRACE](/windows/win32/api/evntrace/ns-evntrace-event_trace)

[EVENT_TRACE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)

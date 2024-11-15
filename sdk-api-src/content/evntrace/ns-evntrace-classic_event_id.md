---
UID: NS:evntrace._CLASSIC_EVENT_ID
title: CLASSIC_EVENT_ID (evntrace.h)
description:
  Identifies the kernel event for which you want to enable call stack tracing.
helpviewer_keywords:
  [
    "*PCLASSIC_EVENT_ID",
    "CLASSIC_EVENT_ID",
    "CLASSIC_EVENT_ID structure [ETW]",
    "PCLASSIC_EVENT_ID",
    "PCLASSIC_EVENT_ID structure pointer [ETW]",
    "_CLASSIC_EVENT_ID",
    "etw.classic_event_id",
    "evntrace/CLASSIC_EVENT_ID",
    "evntrace/PCLASSIC_EVENT_ID",
  ]
old-location: etw\classic_event_id.htm
tech.root: ETW
ms.assetid: cbd77002-466b-40e6-85a5-cd872aef7d51
ms.date: 10/21/2024
ms.keywords:
  "*PCLASSIC_EVENT_ID, CLASSIC_EVENT_ID, CLASSIC_EVENT_ID structure [ETW],
  PCLASSIC_EVENT_ID, PCLASSIC_EVENT_ID structure pointer [ETW],
  _CLASSIC_EVENT_ID, etw.classic_event_id, evntrace/CLASSIC_EVENT_ID,
  evntrace/PCLASSIC_EVENT_ID"
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
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames: CLASSIC_EVENT_ID, *PCLASSIC_EVENT_ID
req.redist:
ms.custom: 19H1
f1_keywords:
  - _CLASSIC_EVENT_ID
  - evntrace/_CLASSIC_EVENT_ID
  - PCLASSIC_EVENT_ID
  - evntrace/PCLASSIC_EVENT_ID
  - CLASSIC_EVENT_ID
  - evntrace/CLASSIC_EVENT_ID
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
  - CLASSIC_EVENT_ID
---

# CLASSIC_EVENT_ID structure

## -description

Identifies the kernel event for which you want to enable call stack tracing. Used with the [TraceStackTracingInfo](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) class of
[TraceSetInformation](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation).

## -struct-fields

### -field EventGuid

The GUID that identifies the kernel event class.

### -field Type

The event type that identifies the event within the kernel event class to enable.

### -field Reserved

Reserved.

## -remarks

Useful values for the EventGuid and Type fields can be determined from consulting the WMI classes in the `root\wmi` namespace. You can also find these values in `wmicore.mof` (where they are originally defined), or see [NT Kernel Logger Constants](/windows/win32/etw/nt-kernel-logger-constants).

### Examples

To enable the [read](/windows/desktop/ETW/diskio-typegroup1) event type for [disk IO](/windows/desktop/ETW/diskio) events, set **GUID** to `3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c` and **Type** to 10.

To enable the [context switch](/windows/win32/etw/cswitch) event type for [thread](/windows/win32/etw/thread-v2) events, set **GUID** to `3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c` and **Type** to 36.

## -see-also

[TraceSetInformation](/windows/desktop/ETW/tracesetinformation)

[TRACE_QUERY_INFO_CLASS](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

[NT Kernel Logger Constants](/windows/win32/etw/nt-kernel-logger-constants)

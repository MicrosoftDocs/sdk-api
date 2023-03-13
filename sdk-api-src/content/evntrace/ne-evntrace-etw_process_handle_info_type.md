---
UID: NE:evntrace._ETW_PROCESS_HANDLE_INFO_TYPE
title: ETW_PROCESS_HANDLE_INFO_TYPE (evntrace.h)
description:
  Specifies the operation that will be performed on a trace processing session.
helpviewer_keywords:
  [
    "ETW_PROCESS_HANDLE_INFO_TYPE",
    "ETW_PROCESS_HANDLE_INFO_TYPE enumeration [ETW]",
    "EtwQueryPartitionInformation",
    "EtwQueryProcessHandleInfoMax",
    "etw.etw_process_handle_info_type",
    "evntrace/ETW_PROCESS_HANDLE_INFO_TYPE",
    "evntrace/EtwQueryPartitionInformation",
    "evntrace/EtwQueryProcessHandleInfoMax",
  ]
old-location: etw\etw_process_handle_info_type.htm
tech.root: ETW
ms.assetid: 92932E4C-0A06-4CDE-B14B-BF53226E133B
ms.date: 12/05/2018
ms.keywords:
  ETW_PROCESS_HANDLE_INFO_TYPE, ETW_PROCESS_HANDLE_INFO_TYPE enumeration [ETW],
  EtwQueryPartitionInformation, EtwQueryProcessHandleInfoMax,
  etw.etw_process_handle_info_type, evntrace/ETW_PROCESS_HANDLE_INFO_TYPE,
  evntrace/EtwQueryPartitionInformation, evntrace/EtwQueryProcessHandleInfoMax
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: ETW_PROCESS_HANDLE_INFO_TYPE
req.redist:
ms.custom: 19H1
f1_keywords:
  - _ETW_PROCESS_HANDLE_INFO_TYPE
  - evntrace/_ETW_PROCESS_HANDLE_INFO_TYPE
  - ETW_PROCESS_HANDLE_INFO_TYPE
  - evntrace/ETW_PROCESS_HANDLE_INFO_TYPE
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - evntrace.h
api_name:
  - ETW_PROCESS_HANDLE_INFO_TYPE
---

# ETW_PROCESS_HANDLE_INFO_TYPE enumeration

## -description

Specifies the operation that will be performed on a trace processing session.
Used with the
[QueryTraceProcessingHandle](/windows/win32/api/evntrace/nf-evntrace-querytraceprocessinghandle)
function.

Specifies what kind of operation will be done on a handle. currently used with the <a href="/windows/desktop/ETW/querytraceprocessinghandle">QueryTraceProcessingHandle</a> function.

## -enum-fields

### -field EtwQueryPartitionInformation:1

Used to query partition identifying information. _InBuffer_ should be Null.
_OutBuffer_ should be large enough to hold the returned
[ETW_TRACE_PARTITION_INFORMATION](/windows/win32/api/evntrace/ns-evntrace-etw_trace_partition_information)
structure. Note that this will only return a non-zero structure when the queried
handle is for a trace file generated from a non-host partition on Windows 10,
version 1709 or later.

### -field EtwQueryPartitionInformationV2:2

This is the same as **EtwQueryPartitionInformation**, except that it returns an
`ETW_TRACE_PARTITION_INFORMATION_V2` structure which has string partition IDs.

### -field EtwQueryLastDroppedTimes:3

Returns a ULONG stream count followed by an array of LARGE_INTEGER timestamps,
indexed by CPU number, of the last event dropped on each CPU stream. The zero
timestamp indicates that the CPU stream never dropped any events. The timestamps
use the clock type specified by the trace configuration (e.g. QPC, System Time,
or CPU counter).

### -field EtwQueryProcessHandleInfoMax

Marks the last value in the enumeration for testing purposes. Should not be
used.

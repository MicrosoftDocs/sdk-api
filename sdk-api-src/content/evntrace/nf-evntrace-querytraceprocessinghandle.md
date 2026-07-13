---
UID: NF:evntrace.QueryTraceProcessingHandle
title: QueryTraceProcessingHandle function (evntrace.h)
description:
  Retrieves information about an ETW trace processing session opened by
  OpenTrace.
helpviewer_keywords:
  [
    "QueryTraceProcessingHandle",
    "QueryTraceProcessingHandle function [ETW]",
    "etw.querytraceprocessinghandle",
    "evntrace/QueryTraceProcessingHandle",
  ]
old-location: etw\querytraceprocessinghandle.htm
tech.root: ETW
ms.assetid: 87666275-8752-4EC8-9C01-16D36AE4C5E8
ms.date: 07/15/2024
ms.keywords:
  QueryTraceProcessingHandle, QueryTraceProcessingHandle function [ETW],
  etw.querytraceprocessinghandle, evntrace/QueryTraceProcessingHandle
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server, version 1709
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - QueryTraceProcessingHandle
  - evntrace/QueryTraceProcessingHandle
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-eventing-consumer-l1-1-2.dll
 - api-ms-win-eventing-consumer-l1-1-1.dll
 - AdvAPI32.dll
 - Sechost.dll
api_name:
  - QueryTraceProcessingHandle
---

# QueryTraceProcessingHandle function

## -description

Retrieves information about an ETW trace processing session opened by
[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea).

## -parameters

### -param ProcessingHandle [in]

A valid handle created with
[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea) that the data
should be queried from.

### -param InformationClass [in]

An
[ETW_PROCESS_HANDLE_INFO_TYPE](/windows/win32/api/evntrace/ne-evntrace-etw_process_handle_info_type)
value that specifies what kind of operation will be done on the handle.

### -param InBuffer [in, optional]

Reserved for future use. May be null.

### -param InBufferSize [in]

Size in bytes of the _InBuffer_.

### -param OutBuffer [out, optional]

Buffer provided by the caller to receive output data.

### -param OutBufferSize [in]

Size in bytes of _OutBuffer._

### -param ReturnLength [out]

The size in bytes of the data that the API wrote into _OutBuffer_. Used for
variable length returns.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes).

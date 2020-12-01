---
UID: NS:avrfsdk._AVRF_HANDLE_OPERATION
title: AVRF_HANDLE_OPERATION (avrfsdk.h)
description: Contains information required to collect handle trace information.
helpviewer_keywords: ["*PAVRF_HANDLE_OPERATION","AVRF_HANDLE_OPERATION","AVRF_HANDLE_OPERATION structure [Windows API]","avrfsdk/AVRF_HANDLE_OPERATION","base.avrf_handle_operation","winprog.avrf_handle_operation"]
old-location: winprog\avrf_handle_operation.htm
tech.root: winprog
ms.assetid: 9268d24d-5000-4ac5-a3c5-895613ccbb9a
ms.date: 12/05/2018
ms.keywords: '*PAVRF_HANDLE_OPERATION, AVRF_HANDLE_OPERATION, AVRF_HANDLE_OPERATION structure [Windows API], avrfsdk/AVRF_HANDLE_OPERATION, base.avrf_handle_operation, winprog.avrf_handle_operation'
req.header: avrfsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AVRF_HANDLE_OPERATION, *PAVRF_HANDLE_OPERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AVRF_HANDLE_OPERATION
 - avrfsdk/_AVRF_HANDLE_OPERATION
 - PAVRF_HANDLE_OPERATION
 - avrfsdk/PAVRF_HANDLE_OPERATION
 - AVRF_HANDLE_OPERATION
 - avrfsdk/AVRF_HANDLE_OPERATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Avrfsdk.h
api_name:
 - AVRF_HANDLE_OPERATION
---

# AVRF_HANDLE_OPERATION structure


## -description

Contains information required to collect handle trace information.

## -struct-fields

### -field Handle

The handle to the heap in which handle traces are being enumerated.

### -field ProcessId

A unique identifier associated with the process in which the application is running.

### -field ThreadId

A unique identifier of the thread (returned by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a> function) that has performed an operation on the given handle.

### -field OperationType

One of the constants in the <a href="/windows/desktop/api/avrfsdk/ne-avrfsdk-ehandle_trace_operations">eHANDLE_TRACE_OPERATIONS</a> enum that indicate whether the handle operation is                  an open(create), close, or invalid.

### -field Spare0

The alignment of the structure on a natural boundary even if the user has changed the size of the original structure.

### -field BackTraceInformation

Identifies the <a href="/windows/desktop/api/avrfsdk/ns-avrfsdk-avrf_backtrace_information">AVRF_BACKTRACE_INFORMATION</a> structure containing information required for completing the enumeration of handles.

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>
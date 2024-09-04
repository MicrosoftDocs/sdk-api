---
UID: NF:evntrace.ProcessTraceBufferIncrementReference
tech.root: ETW
title: ProcessTraceBufferIncrementReference
ms.date: 07/12/2024
targetos: Windows
description: Called during the BufferCallback on the provided Buffer to prevent it from being freed until the caller is done with it.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.header: evntrace.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Advapi32.dll
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 2022 Update
req.target-min-winversvr: Windows Server 2022
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
  - DllExport
api_location:
 - evntrace.h
api_name:
 - ProcessTraceBufferIncrementReference
f1_keywords:
 - ProcessTraceBufferIncrementReference
 - evntrace/ProcessTraceBufferIncrementReference
dev_langs:
 - c++
helpviewer_keywords:
 - ProcessTraceBufferIncrementReference
---

# ProcessTraceBufferIncrementReference function

## -description

Called during the [BufferCallback](nc-evntrace-petw_buffer_callback.md) on the provided Buffer to prevent it from being freed until the caller is done with it.

## -parameters

### -param TraceHandle

The processing session that this *Buffer* came from.

### -param Buffer

The buffer to reference. This buffer must have been obtained by a call to the [PETW_BUFFER_CALLBACK](nc-evntrace-petw_buffer_callback.md) callback.

## -returns

Win32 Error Code. Possible codes may include ERROR_INVALID_PARAMETER and ERROR_OUTOFMEMORY.

## -remarks

If **ProcessTraceBufferIncrementReference** is not called on a Buffer during the [PETW_BUFFER_CALLBACK](nc-evntrace-petw_buffer_callback.md) then the memory is no longer accessible after the [PETW_BUFFER_CALLBACK](nc-evntrace-petw_buffer_callback.md) returns.

The caller is responsible for calling **ProcessTraceBufferDecrementReference** on the Buffer once they are done with it. [ProcessTrace](nf-evntrace-processtrace.md) will not return until this has been done for every buffer that was incremented.

**ProcessTraceBufferIncrementReference** is not supported for buffers provided by a processing session opened by [OpenTraceFromBufferStream](nf-evntrace-opentracefrombufferstream.md).

## -see-also

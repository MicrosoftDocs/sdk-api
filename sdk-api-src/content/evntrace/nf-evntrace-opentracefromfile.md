---
UID: NF:evntrace.OpenTraceFromFile
tech.root: ETW
title: OpenTraceFromFile
ms.date: 07/12/2024
targetos: Windows
description: Creates a trace processing session to process a Tracelog .etl file.
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
 - OpenTraceFromFile
f1_keywords:
 - OpenTraceFromFile
 - evntrace/OpenTraceFromFile
dev_langs:
 - c++
helpviewer_keywords:
 - OpenTraceFromFile
---

# OpenTraceFromFile function

## -description

Creates a trace processing session to process a Tracelog .etl file.

## -parameters

### -param LogFileName

The path of the Tracelog .etl file to process.

### -param Options

Configuration options for this processing session. See [ETW_OPEN_TRACE_OPTIONS](ns-evntrace-etw_open_trace_options.md) for more details.

### -param LogFileHeader

Header information for the log file. See [TRACE_LOGFILE_HEADER](ns-evntrace-trace_logfile_header.md) for more details.

## -returns

A TRACEHANDLE that is used to identify this processing session. Typically passed to [ProcessTrace](nf-evntrace-processtrace.md) to begin processing and to [CloseTrace](nf-evntrace-closetrace.md) to end processing.

## -remarks

Once [ProcessTrace](nf-evntrace-processtrace.md) is called on the returned **TRACEHANDLE**, this will immediately begin processing the file and calling the callbacks specified in *Options*.

## -see-also


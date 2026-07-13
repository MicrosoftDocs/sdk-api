---
UID: NS:evntrace.ETW_BUFFER_CALLBACK_INFORMATION
tech.root: ETW
title: ETW_BUFFER_CALLBACK_INFORMATION
ms.date: 11/21/2022
targetos: Windows
description: Provided to the BufferCallback as the *ConsumerInfo* parameter and provides details on the current processing session.
req.construct-type: structure
req.ddi-compliance: 
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.header: evntrace.h
req.include-header: 
req.kmdf-ver: 
req.lib:
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.target-type: Windows
req.typenames: ETW_BUFFER_CALLBACK_INFORMATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntrace.h
api_name:
 - ETW_BUFFER_CALLBACK_INFORMATION
f1_keywords:
 - ETW_BUFFER_CALLBACK_INFORMATION
 - evntrace/ETW_BUFFER_CALLBACK_INFORMATION
dev_langs:
 - c++
helpviewer_keywords:
 - ETW_BUFFER_CALLBACK_INFORMATION
---

# ETW_BUFFER_CALLBACK_INFORMATION structure

## -description

Provided to the BufferCallback as the *ConsumerInfo* parameter and provides details on the current processing session.

## -struct-fields

### -field TraceHandle

The TraceHandle for this processing session.

### -field LogfileHeader

[TRACE_LOGFILE_HEADER](ns-evntrace-trace_logfile_header.md) structure containing trace processing status (previously-existing structure).

### -field BuffersRead

The count of how many buffers have been processed up to this point.

## -remarks

## -see-also

---
UID: NS:evntrace.ETW_BUFFER_HEADER
tech.root: ETW
title: ETW_BUFFER_HEADER
ms.date: 11/21/2022
targetos: Windows
description: The header structure of an ETW buffer.
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
req.typenames: ETW_BUFFER_HEADER
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntrace.h
api_name:
 - ETW_BUFFER_HEADER
f1_keywords:
 - ETW_BUFFER_HEADER
 - evntrace/ETW_BUFFER_HEADER
dev_langs:
 - c++
helpviewer_keywords:
 - ETW_BUFFER_HEADER
---

# ETW_BUFFER_HEADER structure

## -description

The header structure of an ETW buffer.

## -struct-fields

### -field Reserved1

Reserved.

### -field TimeStamp

The time when the buffer was flushed. It will be in the raw clock type of the session from which the buffer was collected (for example, QueryPerformanceCounter, CPU timestamp counter, or GetSystemTimeAsFileTime).

### -field Reserved2

Reserved.

### -field ClientContext

Contains information about the processor and logger that generated this buffer. See [ETW_BUFFER_CONTEXT](ns-evntrace-etw_buffer_context.md).

### -field Reserved3

### -field FilledBytes

The size of the valid data in the buffer. This is the size of the ETW_BUFFER_HEADER and the event data. When a buffer is copied, it is common to only allocate enough memory to store the valid data (for example, only FilledBytes bytes are allocated and copied), so recipients of a buffer should not read beyond this offset

### -field Reserved4

Reserved.

## -remarks

## -see-also

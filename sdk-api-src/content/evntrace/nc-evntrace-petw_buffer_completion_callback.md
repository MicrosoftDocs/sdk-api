---
UID: NC:evntrace.PETW_BUFFER_COMPLETION_CALLBACK
tech.root: ETW
title: PETW_BUFFER_COMPLETION_CALLBACK
ms.date: 11/21/2022
targetos: Windows
description: Function definition for the callback that will be fired when ProcessTraceAddBufferToBufferStream is finished with a buffer. This callback should typically free the buffer as appropriate
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
req.lib:
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - evntrace.h
api_name:
 - PETW_BUFFER_COMPLETION_CALLBACK
f1_keywords:
 - PETW_BUFFER_COMPLETION_CALLBACK
 - evntrace/PETW_BUFFER_COMPLETION_CALLBACK
dev_langs:
 - c++
helpviewer_keywords:
 - PETW_BUFFER_COMPLETION_CALLBACK
---

# PETW_BUFFER_COMPLETION_CALLBACK callback function

## -description

Function definition for the callback that will be fired when [ProcessTraceAddBufferToBufferStream](nf-evntrace-processtraceaddbuffertobufferstream.md) is finished with a buffer. This callback should typically free the buffer as appropriate

## -parameters

### -param Buffer

Pointer to the raw ETW buffer

### -param CallbackContext

User defined context passed in as BufferCompletionContext to [OpenTraceFromBufferStream](nf-evntrace-opentracefrombufferstream.md).

## -remarks

## -see-also


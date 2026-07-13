---
UID: NF:relogger.ITraceEvent.SetThreadTimes
tech.root: ETW
title: ITraceEvent::SetThreadTimes (relogger.h)
ms.date: 12/01/2022
ms.keywords: SetThreadTimes
targetos: Windows
description: Sets the thread times in the current thread.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: relogger.h
req.idl: Relogger.idl
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - relogger.h
api_name:
 - ITraceEvent::SetThreadTimes
f1_keywords:
 - ITraceEvent::SetThreadTimes
 - relogger/ITraceEvent::SetThreadTimes
dev_langs:
 - c++
helpviewer_keywords:
 - SetThreadTimes
---

# ITraceEvent::SetThreadTimes (relogger.h)

## -description

Sets the thread times in the current thread.

## -parameters

### -field KernelTime

The time executed in kernel mode, in 100-nanosecond intervals.

### -field UserTime

The time executed in user mode, in 100-nanosecond intervals.

## -returns

Type: **HRESULT**

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also

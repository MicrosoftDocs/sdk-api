---
UID: NF:traceloggingprovider.TraceLoggingUnregister
title: TraceLoggingUnregister
ms.date: 5/7/2019
ms.keywords: TraceLoggingUnregister
targetos: Windows
req.assembly:
req.construct-type: function
req.ddi-compliance:
req.dll:
req.header: traceloggingprovider.h
req.idl:
req.include-header:
req.irql:
req.kmdf-ver:
req.lib:
req.max-support:
req.namespace:
req.redist:
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type:
req.type-library:
req.umdf-ver:
req.unicode-ansi:
f1_keywords:
  - TraceLoggingUnregister
  - traceloggingprovider/TraceLoggingUnregister
dev_langs:
  - c++
topic_type:
  - apiref
api_type:
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingUnregister
---

## -description

Unregisters a TraceLogging provider.

## -parameters

### -param hProvider

A handle to the provider to unregister.

## -remarks

You must unregister your provider before it is unloaded or deleted. Otherwise,
the ETW callback routines will fail and have unpredictable results.

In regards to thread safety, do not overlap calls to
[TraceLoggingRegister](nf-traceloggingprovider-traceloggingregister.md) and
**TraceLoggingUnregister** with calls to other TraceLogging APIs using the same
provider handle. In particular, the call to **TraceLoggingRegister** must return
before you call **TraceLoggingWrite** or **TraceLoggingUnregister**. Calls to
other APIs must also complete before you call **TraceLoggingUnregister**.

In addition, you must not call **TraceLoggingRegister** on a handle that is
already registered or for a handle that could be in the process of being
registered or unregistered on another thread.

## -see-also

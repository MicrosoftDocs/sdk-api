---
UID: NF:traceloggingprovider.TraceLoggingRegister
title: TraceLoggingRegister
ms.date: 5/7/2019
ms.keywords: TraceLoggingRegister
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
  - TraceLoggingRegister
  - traceloggingprovider/TraceLoggingRegister
dev_langs:
  - c++
topic_type:
  - apiref
api_type:
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingRegister
---

## -description

Registers a TraceLogging provider so that it can be used for to log events.

## -parameters

### -param hProvider

The handle of the provider to register.

## -returns

If you call this function from user mode code, the function returns a HRESULT.
Use the `SUCCEEDED()` macro to determine if the function succeeds.

If you call this function from kernel mode code, the function returns a
NTSTATUS. Use the `NT_SUCCESS()` macro to determine if the function succeeds.

## -remarks

Call this function to register your provider. You need to register before you
can use it. If you attempt to register a provider that is already registered,
the results are unpredictable. You can unregister a handler and then register it
again if necessary. If registration does fail, all write and unregister commands
will have no effect.

Use the `SUCCEEDED` (user-mode) or `NT_SUCCESS` (kernel-mode) macro to see if
registration was successful.

## -see-also

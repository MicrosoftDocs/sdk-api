---
UID: NF:traceloggingprovider.TraceLoggingRegisterEx
title: TraceLoggingRegisterEx function (traceloggingprovider.h)
description:
  Registers a TraceLogging provider with callback so that it can be used for to
  log events.
helpviewer_keywords:
  [
    "TraceLoggingRegisterEx",
    "TraceLoggingRegisterEx function",
    "tracelogging.traceloggingregisterex",
    "traceloggingprovider/TraceLoggingRegisterEx",
  ]
old-location: tracelogging\traceloggingregisterex.htm
tech.root: tracelogging
ms.assetid: E64B3855-A43B-489B-8A73-930D65FA5F79
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingRegisterEx, TraceLoggingRegisterEx function,
  tracelogging.traceloggingregisterex,
  traceloggingprovider/TraceLoggingRegisterEx
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: Advapi32.lib
req.dll: N/A
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - TraceLoggingRegisterEx
  - traceloggingprovider/TraceLoggingRegisterEx
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - N/A
api_name:
  - TraceLoggingRegisterEx
---

# TraceLoggingRegisterEx function

## -description

Registers a TraceLogging provider with callback so that it can be used for to
log events.

## -parameters

### -param unnamedParam1 [in, out]

The handle of the provider to register.

### -param unnamedParam2 [in, optional]

Callback that ETW calls to notify you when a session enables or disables your
provider. Defaults to **NULL**.

### -param unnamedParam3 [in, optional]

Provider-defined context data to pass to the callback when the provider is
enabled or disabled. Defaults to **NULL**.

## -returns

If you call this function from user mode code, the function returns a HRESULT.
Use the SUCCEEDED() macro to determine if the function succeeds.

If you call this function from kernel mode code, the function returns a
NTSTATUS. Use the NT_SUCCESS() macro to determine if the function succeeds.

## -remarks

Call this function to register your provider. You need to register before you
can use it. If you attempt to register a provider that is already registered,
the registration will fail. You can unregister a handler and the register it
again if necessary. If registration does fail, all write and unregister commands
will have no effect.

Use the `SUCCEEDED` (user-mode) or `NT_SUCCESS` (kernel-mode) macro to see if
registration was successful.

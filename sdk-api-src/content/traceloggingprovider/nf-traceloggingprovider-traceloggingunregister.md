---
UID: NF:traceloggingprovider.TraceLoggingUnregister
title: TraceLoggingUnregister
description: Unregisters a TraceLogging provider.
ms.date: 06/06/2022
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
req.lib: Advapi32.lib
req.max-support:
req.namespace:
req.redist:
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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

The handle of the TraceLogging provider to unregister.

## -remarks

When a component starts running, any TraceLogging provider handle in the
component will be in an unregistered state and any attempts to use the
provider's handle to generate events will be silently ignored. Before the
provider can write any events, you need to register the provider using
[**TraceLoggingRegister**](./nf-traceloggingprovider-traceloggingregister.md).
You will typically do this during component startup. At component shutdown,
unregister the provider by calling **TraceLoggingUnregister**, e.g. before
returning from `main`, `wmain`, or `WinMain`, in `DllMain(DLL_PROCESS_DETACH)`,
before returning from a failed `DriverEntry`, or in the driver Unload routine.

**TraceLoggingRegister** is not thread-safe with regards to other calls to
**TraceLoggingRegister** or **TraceLoggingUnregister** on the same handle. Do
not call **TraceLoggingRegister** if it is possible that another thread might
call **TraceLoggingRegister** or **TraceLoggingUnregister** on the same handle
at the same time.

If **TraceLoggingRegister** fails, the provider handle will remain unregistered
and all uses of the provider handle will be safe no-ops. In particular, it is a
safe no-op to call **TraceLoggingWrite** or **TraceLoggingUnregister** with an
unregistered provider handle.

> [!IMPORTANT]
> If your DLL or driver calls `TraceLoggingRegister` on a provider
> handle, it **must** call `TraceLoggingUnregister` on that provider handle
> before the DLL or driver unloads. If a DLL unloads without calling
> `TraceLoggingUnregister`, the process may subsequently crash. If a driver
> unloads without calling `TraceLoggingUnregister`, the system may subsequently
> crash. The `TraceLoggingRegister` function establishes an ETW configuration
> callback, and `TraceLoggingUnregister` cancels the callback. If the callback
> is not cancelled and the module unloads, a crash will occur the next time ETW
> tries to invoke the callback.

## -see-also

[TraceLoggingRegister](./nf-traceloggingprovider-traceloggingregister.md)

[EventUnregister](../evntprov/nf-evntprov-eventunregister.md)

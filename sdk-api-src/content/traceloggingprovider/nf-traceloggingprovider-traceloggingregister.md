---
UID: NF:traceloggingprovider.TraceLoggingRegister
title: TraceLoggingRegister
description:
  Registers a TraceLogging provider so that it can be used to log events.
ms.date: 06/06/2022
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

Registers a TraceLogging provider so that it can be used to log events. The
registration is valid until the provider is unregistered or the process exits.

## -parameters

### -param hProvider

The handle of the TraceLogging provider to register. The handle must not already
be registered.

## -returns

If you call this function from user-mode code, the function returns an
`HRESULT`. Use the `SUCCEEDED()` macro to determine whether the function
succeeds.

If you call this function from kernel-mode code, the function returns an
`NTSTATUS`. Use the `NT_SUCCESS()` macro to determine whether the function
succeeds.

> [!NOTE]
> The error code returned by **TraceLoggingRegister** is primarily
> intended for use in debugging and diagnostic scenarios. Most production code
> should continue to run even if an ETW provider failed to register, so release
> builds should usually ignore the error code returned by
> **TraceLoggingRegister**.

## -remarks

When a component starts running, any TraceLogging provider handle in the
component will be in an unregistered state and any attempts to use the
provider's handle to generate events will be silently ignored. Before the
provider can write any events, you need to register the provider using
**TraceLoggingRegister**. You will typically do this during component startup,
e.g. in `main`, `wmain`, `WinMain`, `DllMain(DLL_PROCESS_ATTACH)`, or
`DriverEntry`. At component shutdown, unregister the provider by calling
[TraceLoggingUnregister](./nf-traceloggingprovider-traceloggingunregister.md).

Do not call **TraceLoggingRegister** on a provider handle that is already
registered. You can unregister a handle and then register it again if necessary,
though repeatedly registering and unregistering the handle can cause performance
issues and should be avoided (i.e. do not register, write a few events, and then
unregister; instead, register once at component startup and unregister at
component shutdown).

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
> If your DLL or driver calls **TraceLoggingRegister** on a
> provider handle, it **must** call **TraceLoggingUnregister** on that provider
> handle before the DLL or driver unloads. If a DLL unloads without calling
> **TraceLoggingUnregister**, the process may subsequently crash. If a driver
> unloads without calling **TraceLoggingUnregister**, the system may
> subsequently crash. The **TraceLoggingRegister** function establishes an ETW
> configuration callback, and **TraceLoggingUnregister** cancels the callback.
> If the callback is not cancelled and the module unloads, a crash will occur
> the next time ETW tries to invoke the callback.

> [!WARNING]
> If your driver calls **TraceLoggingRegister** and then encounters
> an error during _DriverEntry_, it must call **TraceLoggingUnregister** before
> returning the error from _DriverEntry_. Normal driver cleanup routines will
> not be called if the driver returns an error from _DriverEntry_, and failure
> to call **TraceLoggingUnregister** will cause the system to crash.

**TraceLoggingRegister** does the following:

- Calls **EventRegister** to open the connection to ETW.
- If **EventRegister** succeeds, calls
  [TraceLoggingSetInformation](./nf-traceloggingprovider-traceloggingsetinformation.md)
  with _InformationClass_
  [EventProviderSetTraits](../evntprov/ne-evntprov-event_info_class.md) to
  configure the provider for TraceLogging support.

A call to **TraceLoggingRegister** is the same as a call to
[**TraceLoggingRegisterEx**](./nf-traceloggingprovider-traceloggingregisterex.md)
with NULL for the _callback_ and _context_ parameters. Use
**TraceLoggingRegisterEx** if you need to receive an
[ETW Enable Callback](../evntprov/nc-evntprov-penablecallback.md) when sessions
enable or disable your provider.

## -see-also

[EventRegister](../evntprov/nf-evntprov-eventregister.md)

[TraceLoggingRegisterEx](./nf-traceloggingprovider-traceloggingregisterex.md)

[TraceLoggingUnregister](./nf-traceloggingprovider-traceloggingunregister.md)

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)

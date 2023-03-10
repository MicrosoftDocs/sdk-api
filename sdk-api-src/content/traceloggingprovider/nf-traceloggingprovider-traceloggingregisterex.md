---
UID: NF:traceloggingprovider.TraceLoggingRegisterEx
title: TraceLoggingRegisterEx function (traceloggingprovider.h)
description:
  Registers a TraceLogging provider so that it can be used to log events,
  specifying an ETW enable callback.
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
ms.date: 06/06/2022
ms.keywords:
  TraceLoggingRegisterEx, TraceLoggingRegisterEx function,
  tracelogging.traceloggingregisterex,
  traceloggingprovider/TraceLoggingRegisterEx
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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

Registers a TraceLogging provider so that it can be used to log events,
specifying an ETW enable callback. The registration is valid until the provider
is unregistered or the process exits.

## -parameters

### -param hProvider [in, out]

The handle of the TraceLogging provider to register. The handle must not already
be registered.

### -param pEnableCallback [in, optional]

[ETW Enable Callback](../evntprov/nc-evntprov-penablecallback.md) that will be
invoked when a trace session enables or disables your provider.

### -param pCallbackContext [in, optional]

Optional provider-defined context pointer to pass to the callback.

## -returns

If you call this function from user-mode code, the function returns an
`HRESULT`. Use the `SUCCEEDED()` macro to determine whether the function
succeeds.

If you call this function from kernel-mode code, the function returns an
`NTSTATUS`. Use the `NT_SUCCESS()` macro to determine whether the function
succeeds.

> [!NOTE]
> The error code returned by TraceLoggingRegisterEx is primarily
> intended for use in debugging and diagnostic scenarios. Most production code
> should continue to run even if an ETW provider failed to register, so release
> builds should usually ignore the error code returned by
> TraceLoggingRegisterEx.

## -remarks

See [TraceLoggingRegister](./nf-traceloggingprovider-traceloggingregister.md)
for details on registering providers. See
[ETW Enable Callback](../evntprov/nc-evntprov-penablecallback.md) for details on
the callback behavior.

**TraceLoggingRegisterEx** does the following:

- Calls **EventRegister** to open the connection to ETW.
- If **EventRegister** succeeds, calls
  [TraceLoggingSetInformation](./nf-traceloggingprovider-traceloggingsetinformation.md)
  with _InformationClass_
  [EventProviderSetTraits](../evntprov/ne-evntprov-event_info_class.md) to
  configure the provider for TraceLogging support.

A call to
[**TraceLoggingRegister**](./nf-traceloggingprovider-traceloggingregister.md) is
the same as a call to **TraceLoggingRegisterEx** with NULL for the _callback_
and _context_ parameters. Use **TraceLoggingRegisterEx** if you need to receive
an ETW Enable Callback when sessions enable or disable your provider.

## -see-also

[ETW Enable Callback](../evntprov/nc-evntprov-penablecallback.md)

[EventRegister](../evntprov/nf-evntprov-eventregister.md)

[TraceLoggingRegister](./nf-traceloggingprovider-traceloggingregister.md)

[TraceLoggingUnregister](./nf-traceloggingprovider-traceloggingunregister.md)

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)

---
UID: NF:traceloggingprovider.TraceLoggingWrite
title: TraceLoggingWrite macro (traceloggingprovider.h)
description: Emits a TraceLogging event.
helpviewer_keywords:
  [
    "TraceLoggingWrite",
    "TraceLoggingWrite macro",
    "tracelogging.traceloggingwrite",
    "traceloggingprovider/TraceLoggingWrite",
  ]
old-location: tracelogging\traceloggingwrite.htm
tech.root: tracelogging
ms.assetid: BFBC6802-64DC-478E-B09D-F550135994AB
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingWrite, TraceLoggingWrite macro, tracelogging.traceloggingwrite,
  traceloggingprovider/TraceLoggingWrite
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
req.dll:
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - TraceLoggingWrite
  - traceloggingprovider/TraceLoggingWrite
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingWrite
---

# TraceLoggingWrite macro

## -syntax

```cpp
void TraceLoggingWrite(
  [in]            TraceLoggingHProvider hProvider,
  [in]            String eventName,
  [in, optional]   args
);
```

## -description

Emits a TraceLogging event.

## -parameters

### -param hProvider [in]

The handle of the
[TraceLogging provider](./nf-traceloggingprovider-tracelogging_define_provider.md)
to use for writing the event.

### -param eventName [in]

A short and unique name to use for identifying the event. This must be a string
literal and not a variable. It cannot have any embedded `'\0'` characters.

### -param __VA_ARGS__ [in, optional]

Up to 99 additional parameters to configure or add fields to the event. Each
parameter must be one of the
[TraceLogging Wrapper Macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros),
such as [TraceLoggingLevel](./nf-traceloggingprovider-tracelogginglevel.md),
[TraceLoggingKeyword](./nf-traceloggingprovider-traceloggingkeyword.md), or
[TraceLoggingValue](./nf-traceloggingprovider-traceloggingvalue.md).

> [!IMPORTANT]
> ProviderId, Level and Keyword are the primary means for filtering
> events. Other kinds of filtering are possible but have much higher overhead.
> Always assign a non-zero level and keyword to every event.

## -remarks

Each invocation of the **TraceLoggingWrite** macro expands to the code necessary
to write an event to ETW through the specified provider handle.

- **TraceLoggingWrite** checks whether the specified provider is registered. If
  the provider is not
  [registered](./nf-traceloggingprovider-traceloggingregister.md),
  **TraceLoggingWrite** does nothing.
- **TraceLoggingWrite** checks whether any consumer is listening for the event,
  as if by calling
  [**TraceLoggingProviderEnabled**](./nf-traceloggingprovider-traceloggingproviderenabled.md).
  If no consumer is listening for the event, **TraceLoggingWrite** does nothing.
- Otherwise, **TraceLoggingWrite** evaluates the runtime expressions specified
  in the arguments, saves the results, packs the necessary data into an event,
  and calls [EventWriteTransfer](../evntprov/nf-evntprov-eventwritetransfer.md)
  to send the event to ETW.

The generated event will be constructed as follows:

- The event's provider ID, provider name, and provider group will come from the
  _hProvider_ parameter.
- The event's name will come from the _eventName_ parameter.
- In user-mode, the event's activity ID will come from the thread's implicit
  activity ID. In kernel-mode, the event's activity ID will be GUID_NULL.
- The event will not have a related activity ID.
- The event's level will come from the
  [TraceLoggingLevel](./nf-traceloggingprovider-tracelogginglevel.md) argument.
  If no TraceLoggingLevel argument is present, the event's level will be 5
  (WINEVENT_LEVEL_VERBOSE). If more than one TraceLoggingLevel argument is present,
  the last argument will be used. To enable effective event filtering, always
  assign a meaningful non-zero level to every event.
- The event's keyword will come from the
  [TraceLoggingKeyword](./nf-traceloggingprovider-traceloggingkeyword.md)
  argument. If no TraceLoggingKeyword argument is present, the event's keyword
  will be 0 (NONE). If more than one TraceLoggingKeyword argument is present,
  the values will be OR'ed together. To enable effective event filtering, always
  assign a meaningful non-zero keyword to every event.
- Other event attributes may be set by arguments such as
  [TraceLoggingOpcode](./nf-traceloggingprovider-traceloggingopcode.md),
  [TraceLoggingDescription](./nf-traceloggingprovider-traceloggingdescription.md),
  [TraceLoggingEventTag](./nf-traceloggingprovider-traceloggingeventtag.md), or
  [TraceLoggingChannel](./nf-traceloggingprovider-traceloggingchannel.md).
- Event fields can be grouped using
  [TraceLoggingStruct](./nf-traceloggingprovider-traceloggingstruct.md).
- Event fields are added by field arguments like
  [TraceLoggingValue](./nf-traceloggingprovider-traceloggingvalue.md),
  TraceLoggingInt32, TraceLoggingHResult, TraceLoggingString, etc. See
  [TraceLogging Wrapper Macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
  for details.

For example:

```c
TraceLoggingWrite(
    g_hProvider,
    "MyEvent1",
    TraceLoggingLevel(WINEVENT_LEVEL_WARNING), // Levels defined in <winmeta.h>
    TraceLoggingKeyword(MyNetworkingKeyword),
    TraceLoggingString(operationName), // Adds an "operationName" field.
    TraceLoggingHResult(hr, "NetStatus")); // Adds a "NetStatus" field.
```

An invocation of `TraceLoggingWrite(hProvider, "EventName", args...)` can be
thought of as expanding to code like the following:

```c
if (TraceLoggingProviderEnabled(hProvider, eventLevel, eventKeyword))
{
    static const metadata = { GetMetadataFromArgs(args...) };
    EVENT_DATA_DESCRIPTOR data[N] = { GetDataFromArgs(args...) };
    EventWriteTransfer(etwHandle, metadata.desc, NULL, NULL, N, data);
}
```

> [!NOTE]
> Each **TraceLoggingWrite** macro automatically checks
> [**TraceLoggingProviderEnabled**](./nf-traceloggingprovider-traceloggingproviderenabled.md)
> so the event will only be written if a consumer is listening for events from
> the provider. As a result, it is usually unnecessary to directly call
> **TraceLoggingProviderEnabled**. Any runtime expressions in `args...` will be
> evaluated if and only if the event is enabled. Runtime expressions will not be
> evaluated more than once.

If generating complex events, you might get a compiler error indicating that the
line is too long or that the compiler is out of heap space. This occurs when the
**TraceLoggingWrite** macro expands to a line longer than can be supported by
the compiler. If this happens you will need to simplify your event.

The **TraceLoggingWrite** macro uses an array of
[EVENT_DATA_DESCRIPTOR](../evntprov/ns-evntprov-event_data_descriptor.md) to
transfer data to ETW. The maximum number of descriptors accepted by ETW is 128.
Since each parameter may require the use of 0, 1, or 2 descriptors, it is
possible to hit the data descriptor limit (128) before hitting the argument
limit (99).

> [!IMPORTANT]
> Try to avoid large events. ETW is primarily designed for handling
> small events. **TraceLoggingWrite** will silently drop any event that is too
> large. The event's size is based on the total of the event's headers (added by
> the ETW runtime), metadata (i.e. provider name, event name, field names, field
> types), and data (field values). If the event's total size is greater than
> 65535 or if the consumer session is using a buffer size smaller than the
> event's size, the event will not be recorded.

A call to **TraceLoggingWrite** is the same as a call to
[**TraceLoggingWriteActivity**](./nf-traceloggingprovider-traceloggingwriteactivity.md)
with NULL for the _pActivityId_ and _pRelatedActivityId_ parameters. Use
**TraceLoggingWriteActivity** if you need to specify activity IDs for an event.

### Examples

```c
#include <windows.h> // or <wdm.h> for kernel-mode.
#include <winmeta.h> // For event level definitions.
#include <TraceLoggingProvider.h>

TRACELOGGING_DEFINE_PROVIDER( // defines g_hProvider
    g_hProvider,  // Name of the provider handle
    "MyProvider", // Human-readable name of the provider
    // ETW Control GUID: {b3864c38-4273-58c5-545b-8b3608343471}
    (0xb3864c38,0x4273,0x58c5,0x54,0x5b,0x8b,0x36,0x08,0x34,0x34,0x71));

int main(int argc, char* argv[]) // or DriverEntry for kernel-mode.
{
    TraceLoggingRegister(g_hProvider);

    TraceLoggingWrite(
        g_hProvider,
        "MyEvent1",
        TraceLoggingLevel(WINEVENT_LEVEL_WARNING), // Levels defined in <winmeta.h>
        TraceLoggingKeyword(MyEventCategories), // Provider-defined categories
        TraceLoggingString(argv[0], "arg0"), // field name is "arg0"
        TraceLoggingInt32(argc)); // field name is implicitly "argc"

    TraceLoggingUnregister(g_hProvider);
    return 0;
}
```

## -see-also

[EventWriteTransfer](../evntprov/nf-evntprov-eventwritetransfer.md)

[TraceLoggingWriteActivity](./nf-traceloggingprovider-traceloggingwriteactivity.md)

[TraceLogging Wrapper Macros](/windows/win32/tracelogging/tracelogging-wrapper-macros)

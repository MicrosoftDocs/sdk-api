---
UID: NF:traceloggingprovider.TraceLoggingChannel
title: TraceLoggingChannel macro (traceloggingprovider.h)
description: TraceLogging wrapper macro that sets the channel for the event.
helpviewer_keywords:
  [
    "TraceLoggingChannel",
    "TraceLoggingChannel macro",
    "tracelogging.traceloggingchannel",
    "traceloggingprovider/TraceLoggingChannel",
  ]
old-location: tracelogging\traceloggingchannel.htm
tech.root: tracelogging
ms.assetid: E7769335-3A1D-4F0B-86DA-20DA3F7B6733
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingChannel, TraceLoggingChannel macro,
  tracelogging.traceloggingchannel, traceloggingprovider/TraceLoggingChannel
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - TraceLoggingChannel
  - traceloggingprovider/TraceLoggingChannel
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
  - TraceLoggingChannel
---

# TraceLoggingChannel macro

## -syntax

```cpp
void TraceLoggingChannel(
  [in]  int eventChannel
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that sets the channel for the event.

Most TraceLogging events do not need to change the event's default channel and
should not use TraceLoggingChannel.

## -parameters

### -param eventChannel [in]

The channel to which the event should be logged. This is an integer value from 0
to 255.

See [EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md) for details
about the event channel.

## -remarks

`TraceLoggingChannel(eventChannel)` can be used as a parameter to an invocation
of a [TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro.
Most TraceLogging events do not need to change the event's default channel and
should not use **TraceLoggingChannel**.

The eventChannel parameter must be a compile-time constant 0 to 255. If no
`TraceLoggingChannel(n)` arg is provided, the default channel is 11
(WINEVENT_CHANNEL_TRACELOGGING), indicating that this is a normal TraceLogging
event. If multiple `TraceLoggingChannel(n)` args are provided, the value from
the last `TraceLoggingChannel(n)` parameter will be used.

Channels are used in advanced Event Tracing for Windows (ETW) scenarios. These
include writing to system-defined event consumers such as the
[Windows Event Log](/windows/win32/wes/windows-event-log).

> [!WARNING]
> If your provider will run on Windows earlier than Windows 10, do
> not use **TraceLoggingChannel**. For an event to be recognized as
> TraceLogging-compatible by event decoders, it must either have the channel set
> to the default value (11) or it must have been marked as a TraceLogging event
> by the ETW runtime during EventWrite. This event marking is enabled by calling
> EventSetInformation to configure the provider as a TraceLogging provider.
> EventSetInformation in Windows 10 or later enables support for TraceLogging
> events regardless of channel, but earlier versions of Windows require a
> Windows update before they support marking TraceLogging events. For events
> captured on systems without an updated EventSetInformation, channel 11 is the
> only way to recognize a TraceLogging event, so events with other channels may
> not decode correctly.

### TraceLogging and Event Log

In most cases, developers use manifest-based ETW for events that need to be
recorded by Event Log. Event Log is primarily intended to collect low-volume
events that are likely to be useful to the administrator of a system.
Manifest-based ETW works well for this because it supports carefully-curated
events (all events for the component are described in one manifest file) and
because it supports localizable message strings that can help the administrator
know how to react to the event.

Although TraceLogging events do not have message strings and are generally not
centrally-curated, TraceLogging can still be appropriate for some Event Log
scenarios. For example, while events that go to the Windows Logs (Application,
Security, Setup and System) should always have localized message strings and
should always be useful to the system administrator, events recorded in the
Applications and Services Logs can be more technical and can record diagnostic
information. When writing to the Applications and Services Logs, you might want
to use TraceLogging to simplify management of the logged events.

Using TraceLogging events with Windows Event Log is similar to using normal
manifest-based events with Event Log. You still need to create and register a
manifest to define the provider and the channels but you don't need to define
the individual events in the manifest:

- [Write an ETW manifest](/windows/win32/wes/writing-an-instrumentation-manifest)
  that defines your provider and the Event Log channels. The provider in the
  manifest should use the same provider name and provider guid (provider ID) as
  you used in your
  [TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)
  macro. The manifest does not need to include `<event>` or `<template>`
  definitions since TraceLogging events are self-describing.
- In the build process for your component, use
  [Message Compiler (MC.exe)](/windows/win32/wes/message-compiler--mc-exe-) from
  Windows SDK 10.0.22621 or later to compile the manifest. This will generate
  the following files:
  - `ManifestName.h`: C/C++ header containing constant definitions. This will
    define the _ChannelSymbol_ and the _ChannelSymbol_KEYWORD_ constants that
    you will need to use in your TraceLogging events. (The actual names of the
    constants will be different for each channel.)
  - `ManifestName.rc`:
    [Resource Compiler (RC.exe)](/windows/win32/menurc/resource-compiler) script
    that adds the manifest BIN data to a binary (EXE, DLL, or SYS) file. You
    will need to include this resource script into the resources of one of the
    binary files in your component.
  - `ManifestNameTEMP.BIN`, `MSG00001.bin`: manifest BIN data referenced by
    `ManifestName.rc`.
- `#include` the generated `ManifestName.h` file into the code that needs to
  generate TraceLogging events. This will define the _ChannelSymbol_ and
  _ChannelSymbol_KEYWORD_ constants.
  - If you specified the _symbol_ attribute on the `<channel>` or
    `<importChannel>` definition in the manifest, the name of _ChannelSymbol_
    will be the value of your _symbol_ attribute. Otherwise, _ChannelSymbol_
    will be _ProviderSymbol_CHANNEL_ChannelName_ (i.e. it will use the symbol
    from your `<provider>` element and the name from your `<channel>` or
    `<importChannel>` element).
  - The name of _ChannelSymbol_KEYWORD_ is the name of _ChannelSymbol_ followed
    by `_KEYWORD`.
  - The _ChannelSymbol_KEYWORD_ constant is only generated by `MC.exe`
    10.0.22621 or later.
- Each TraceLogging event that is to go to Event Log must use
  `TraceLoggingChannel(ChannelSymbol), TraceLoggingKeyword(ChannelSymbol_KEYWORD)`
  to set the channel and keyword for the event. For example, if my channel's
  symbol is `MY_CHANNEL`, I would add
  `TraceLoggingChannel(MY_CHANNEL), TraceLoggingKeyword(MY_CHANNEL_KEYWORD)` as
  parameters to the `TraceLoggingWrite` macro for the event.
- In order for Event Log to recognize your provider, the information from your
  manifest
  [must be included in the resources](/windows/win32/wes/compiling-an-instrumentation-manifest)
  of a module (DLL, EXE, or SYS file) that will be installed on the target
  system.
- In order for Event Log to receive events from your provider, you must
  [register your manifest](/windows/win32/wes/developing-a-provider) on the
  target system using
  `wevtutil im ManifestFile.man /rf:PathToModuleWithResources.dll` during
  component install. You must also unregister your manifest using
  `wevtutil um ManifestFile.man` during component uninstall.

> [!IMPORTANT]
> If your provider is registered with Event Log, all events
> generated by your provider **must** have a non-zero keyword specified with
> **TraceLoggingKeyword**, even if the event is not intended for Event Log.
> Events with keyword 0 cannot be filtered efficiently and will be delivered to
> Event Log only to be discarded. If Event Log is listening for any events from
> your provider, any event with Keyword 0 will unnecessarily increase Event Log
> overhead.

Example of a TraceLogging event for Event Log:

```c
TraceLoggingWrite(
    g_hMyProvider,
    "MyWarningEventName",
    TraceLoggingChannel(MY_CHANNEL),         // constant from the MC-generated header
    TraceLoggingKeyword(MY_CHANNEL_KEYWORD), // constant from the MC-generated header
    TraceLoggingLevel(WINEVENT_LEVEL_WARNING), // Levels defined in <winmeta.h>
    TraceLoggingKeyword(MyEventCategories), // Additional keywords are ok.
    TraceLoggingHResult(errorCode, "Error"));
```

Additional user-specified keywords can be added to events if appropriate, either
by using multiple **TraceLoggingKeyword** arguments or by specifying multiple
keywords in a single **TraceLoggingKeyword** argument, e.g.
`TraceLoggingKeyword(MY_CHANNEL_KEYWORD | MY_OTHER_KEYWORD)`.

## -see-also

[EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md)

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

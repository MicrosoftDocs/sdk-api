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
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingChannel, TraceLoggingChannel macro,
  tracelogging.traceloggingchannel, traceloggingprovider/TraceLoggingChannel
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that sets the event's channel.

Most TraceLogging events do not need to change the event's default channel and
should not use TraceLoggingChannel.

## -parameters

### -param eventChannel [in]

The channel to which the event should be logged. This is an integer value from 0
to 255.

## -remarks

`TraceLoggingChannel(eventChannel)` can be used as a parameter to an invocation
of a [TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro.
Most TraceLogging events do not need to change the event's default channel and
should not use TraceLoggingChannel.

The eventChannel parameter must be a compile-time constant 0 to 255. If no
`TraceLoggingChannel(n)` arg is provided, the default channel is 11
(WINEVENT_CHANNEL_TRACELOGGING), indicating that this is a normal TraceLogging
event. If multiple `TraceLoggingChannel(n)` args are provided, the value from
the last `TraceLoggingChannel(n)` parameter will be used.

Channels are used in advanced Event Tracing for Windows (ETW) scenarios. These
include writing to system-defined event consumers such as the
[Windows Event Log](/windows/win32/wes/windows-event-log).

> [!Warning]
> If your provider will run on Windows earlier than Windows 10, do
> not use **TraceLoggingChannel**. For an event to be recognized as
> TraceLogging-compatible by event decoders, it must either have the channel set
> to the default value (11) or it must have been marked as a TraceLogging event
> by the ETW runtime during EventWrite. The Windows 10 ETW runtime will
> recognize and mark TraceLogging events regardless of channel, but earlier
> versions of Windows require a system update in order to mark TraceLogging
> events. For events captured on systems without this update, the channel is the
> only way to recognize a TraceLogging event, so events with other channels may
> not decode correctly.

Using TraceLogging events with Windows Event Log is similar to using normal
manifest-based events with Event Log except that you don't need to define each
event in the manifest since TraceLogging events are self-describing. However,
you do still need to create and register a manifest to define the provider and
the channel for Event Log:

- [Write an ETW manifest](/windows/win32/wes/writing-an-instrumentation-manifest)
  that defines your provider and the Event Log channels. The provider in the
  manifest should use the same provider name and provider guid (provider ID) as
  is used in your
  [TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)
  macro. The manifest does not need to include `<event>` or `<template>`
  definitions since TraceLogging events are self-describing.
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
- Each TraceLogging event that is to go to Event Log must use
  **TraceLoggingChannel** to set the correct channel. You can determine the
  correct channel by compiling the manifest with MC.exe and examining the
  generated `.h` file to find the value of the symbol macro corresponding to the
  channel.
- Each TraceLogging event that is to go to Event Log must use
  [TraceLoggingKeyword](./nf-traceloggingprovider-traceloggingkeyword.md) to set
  the channel's keyword bit. You can determine the correct keyword by using
  `0x8000000000000000` for the first channel listed in the provider and using
  the next lower bit for each subsequent channel, e.g. `0x4000000000000000` for
  the second channel listed in the provider, `0x2000000000000000` for the third
  channel, etc.

> [!Important]
> If your provider is registered with Event Log, all events
> generated by your provider must have a non-zero keyword specified with
> **TraceLoggingKeyword**, even if the event is not intended for Event Log.
> Events with keyword 0 cannot be filtered efficiently. If Event Log is
> listening for any events from your provider, any event with Keyword 0 will
> unnecessarily increase Event Log overhead.

## -see-also

[EVENT_DESCRIPTOR](../evntprov/ns-evntprov-event_descriptor.md)

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

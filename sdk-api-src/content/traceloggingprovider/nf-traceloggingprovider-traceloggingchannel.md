---
UID: NF:traceloggingprovider.TraceLoggingChannel
title: TraceLoggingChannel macro (traceloggingprovider.h)
description: Wrapper macro for setting the event's channel.
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

Wrapper macro for setting the event's channel.

## -parameters

### -param eventChannel [in]

The event channel to be logged.

## -remarks

Channels are used in advanced Event Tracing for Windows (ETW) scenarios such as
writing to system-defined event consumers such as the event log. When using
channels, a manifest must be registered with the system to define the provider
and its channels. A manifest for a TraceLogging provider should define the
provider and the channels but should omit the event definitions, since they are
managed by TraceLogging.

The eventChannel parameter must be a compile-time constant 0 to 255. If no
TraceLoggingChannel(n) arg is provided, the default channel level is 11
(WINEVENT_CHANNEL_TRACELOGGING), indicating that this is a normal TraceLogging
event. If multiple TraceLoggingChannel(n) args are provided, the value from the
last TraceLoggingChannel(n) is used.

> [!Warning]
> If your provider will run on Windows earlier than Windows 10, do
> not use TraceLoggingChannel. For an event to be recognized as
> TraceLogging-compatible, it must either have the channel set to 11 or it must
> have been marked by the ETW runtime during EventWrite. The Windows 10 ETW
> runtime will recognize and mark TraceLogging events regardless of channel, but
> earlier versions of Windows require a system update in order to support
> marking TraceLogging events. For events captured on systems without an update,
> the channel is the only way to recognize a TraceLogging event, so events with
> other channels may be harder to decode.

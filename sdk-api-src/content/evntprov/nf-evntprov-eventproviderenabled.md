---
UID: NF:evntprov.EventProviderEnabled
title: EventProviderEnabled function (evntprov.h)
description:
  Determines whether an event provider should generate a particular event based
  on the event's Level and Keyword.
helpviewer_keywords:
  [
    "EventProviderEnabled",
    "EventProviderEnabled function [ETW]",
    "WINEVENT_LEVEL_CRITICAL",
    "WINEVENT_LEVEL_ERROR",
    "WINEVENT_LEVEL_INFO",
    "WINEVENT_LEVEL_VERBOSE",
    "WINEVENT_LEVEL_WARNING",
    "base.eventproviderenabled_func",
    "etw.eventproviderenabled_func",
    "evntprov/EventProviderEnabled",
  ]
old-location: etw\eventproviderenabled_func.htm
tech.root: ETW
ms.assetid: 84c035b1-cdc7-47b7-b887-e5b508f17266
ms.date: 12/05/2018
ms.keywords:
  EventProviderEnabled, EventProviderEnabled function [ETW],
  WINEVENT_LEVEL_CRITICAL, WINEVENT_LEVEL_ERROR, WINEVENT_LEVEL_INFO,
  WINEVENT_LEVEL_VERBOSE, WINEVENT_LEVEL_WARNING,
  base.eventproviderenabled_func, etw.eventproviderenabled_func,
  evntprov/EventProviderEnabled
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Advapi32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - EventProviderEnabled
  - evntprov/EventProviderEnabled
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - Advapi32.dll
  - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
  - KernelBase.dll
  - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
  - API-MS-Win-eventing-provider-l1-1-0.dll
  - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
  - EventProviderEnabled
---

# EventProviderEnabled function

## -description

Determines whether an event provider should generate a particular event based on
the event's Level and Keyword.

Returns **FALSE** if ETW can quickly determine that no session is listening for a specified event from the given provider. Otherwise returns **TRUE**.

## -parameters

### -param RegHandle [in]

Registration handle of the provider. The handle comes from
[EventRegister](/windows/desktop/api/evntprov/nf-evntprov-eventregister).

If _RegHandle_ is **NULL**, **EventProviderEnabled** will return **FALSE**.

### -param Level [in]

An 8-bit number used to describe an event's severity or importance. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
for more information about event level values.

### -param Keyword [in]

A 64-bit bitmask used to indicate an event's membership in a set of event
categories. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
for more information about event keyword values.

## -returns

Returns **FALSE** if ETW can quickly determine that no session is listening for a specified event from the given provider. Otherwise returns **TRUE**.

## -remarks

This API provides a simple way to determine whether an event is enabled (i.e.
whether any event consumer sessions are interested in receiving the event) based
on the provider handle, the event level, and the event keyword.

> [!Note]
> This API performs a conservative quick test. It is possible for this
> API to return true in certain cases where subsequent in-depth filtering would
> determine that no sessions need to record the event.

This API provides functionality similar to the functionality provided by
[EventEnabled](/windows/desktop/api/evntprov/nf-evntprov-eventenabled). When a
provider has access to an event's complete
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor),
the provider should use **EventEnabled**. When a provider has access only to the
event's Level and Keyword, the provider should use **EventProviderEnabled**.

Most event providers will not call **EventProviderEnabled** directly:

- The **EventWrite** APIs include their own **EventProviderEnabled** test and
  return immediately if the event is not enabled.
- Most ETW providers use an ETW framework (e.g. manifests or TraceLogging)
  instead of directly calling **EventWrite** or **EventProviderEnabled**. ETW
  frameworks generally provide their own event-enabled API which should be used
  instead of calling **EventProviderEnabled**.
- ETW framework implementations usually check their own provider state rather
  than calling **EventProviderEnabled**.

For additional details, see
[EventEnabled](/windows/desktop/api/evntprov/nf-evntprov-eventenabled).

## -see-also

[EventEnabled](/windows/desktop/api/evntprov/nf-evntprov-eventenabled)

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

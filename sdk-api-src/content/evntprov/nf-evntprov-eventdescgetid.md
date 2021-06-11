---
UID: NF:evntprov.EventDescGetId
title: EventDescGetId function (evntprov.h)
description: Retrieves the event identifier from the event descriptor.
helpviewer_keywords:
  [
    "EventDescGetId",
    "EventDescGetId function [ETW]",
    "base.eventdescgetid_func",
    "etw.eventdescgetid_func",
    "evntprov/EventDescGetId",
  ]
old-location: etw\eventdescgetid_func.htm
tech.root: ETW
ms.assetid: 33deea6e-27e0-44ae-8d18-e8c854bc1819
ms.date: 12/05/2018
ms.keywords:
  EventDescGetId, EventDescGetId function [ETW], base.eventdescgetid_func,
  etw.eventdescgetid_func, evntprov/EventDescGetId
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
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - EventDescGetId
  - evntprov/EventDescGetId
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - Evntprov.h
api_name:
  - EventDescGetId
---

# EventDescGetId function

## -description

Retrieves the event identifier from the event descriptor.

## -parameters

### -param EventDescriptor [in]

Event descriptor from which to retrieve the event identifier. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

## -returns

The event identifier.

## -remarks

This is a convenience macro for retrieving the member of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

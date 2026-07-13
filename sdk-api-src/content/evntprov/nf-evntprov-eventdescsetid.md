---
UID: NF:evntprov.EventDescSetId
title: EventDescSetId function (evntprov.h)
description: Sets the Id member of the event descriptor.
helpviewer_keywords:
  [
    "EventDescSetId",
    "EventDescSetId function [ETW]",
    "base.eventdescsetid_func",
    "etw.eventdescsetid_func",
    "evntprov/EventDescSetId",
  ]
old-location: etw\eventdescsetid_func.htm
tech.root: ETW
ms.assetid: 1c110ea3-651c-4e2c-9675-64f6975e5fc5
ms.date: 12/05/2018
ms.keywords:
  EventDescSetId, EventDescSetId function [ETW], base.eventdescsetid_func,
  etw.eventdescsetid_func, evntprov/EventDescSetId
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
  - EventDescSetId
  - evntprov/EventDescSetId
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
  - EventDescSetId
---

# EventDescSetId function

## -description

Sets the **Id** member of the event descriptor.

## -parameters

### -param EventDescriptor [in]

Event descriptor to modify. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Id [in]

The event identifier.

## -returns

The modified event descriptor.

## -remarks

This is a convenience macro for setting the member of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

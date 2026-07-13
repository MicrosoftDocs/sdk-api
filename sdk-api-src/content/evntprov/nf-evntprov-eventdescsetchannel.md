---
UID: NF:evntprov.EventDescSetChannel
title: EventDescSetChannel function (evntprov.h)
description: Sets the Channel member of the event descriptor.
helpviewer_keywords:
  [
    "EventDescSetChannel",
    "EventDescSetChannel function [ETW]",
    "base.eventdescsetchannel_func",
    "etw.eventdescsetchannel_func",
    "evntprov/EventDescSetChannel",
  ]
old-location: etw\eventdescsetchannel_func.htm
tech.root: ETW
ms.assetid: 3580935d-ab7e-4409-b4ac-58f3c6019514
ms.date: 12/05/2018
ms.keywords:
  EventDescSetChannel, EventDescSetChannel function [ETW],
  base.eventdescsetchannel_func, etw.eventdescsetchannel_func,
  evntprov/EventDescSetChannel
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
  - EventDescSetChannel
  - evntprov/EventDescSetChannel
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
  - EventDescSetChannel
---

# EventDescSetChannel function

## -description

Sets the **Channel** member of the event descriptor.

## -parameters

### -param EventDescriptor [in]

Event descriptor to modify. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Channel [in]

Channel that defines the category of events to which this event belongs.

## -returns

The modified event descriptor.

## -remarks

This is a convenience macro for setting the member of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

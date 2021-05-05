---
UID: NF:evntprov.EventDescCreate
title: EventDescCreate function (evntprov.h)
description: Sets the values of an event descriptor.
helpviewer_keywords:
  [
    "EventDescCreate",
    "EventDescCreate function [ETW]",
    "base.eventdesccreate_func",
    "etw.eventdesccreate_func",
    "evntprov/EventDescCreate",
  ]
old-location: etw\eventdesccreate_func.htm
tech.root: ETW
ms.assetid: 05ce400e-c2e5-4852-9c41-d98ac2a6b467
ms.date: 12/05/2018
ms.keywords:
  EventDescCreate, EventDescCreate function [ETW], base.eventdesccreate_func,
  etw.eventdesccreate_func, evntprov/EventDescCreate
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
  - EventDescCreate
  - evntprov/EventDescCreate
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
  - EventDescCreate
---

# EventDescCreate function

## -description

Sets the values of an event descriptor.

## -parameters

### -param EventDescriptor [out]

Event descriptor whose member values are set to those of the remaining
parameters. For details, see
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Id [in]

Event identifier. The value is used to set the **Id** member of
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Version [in]

Version of the event. The value is used to set the **Version** member of
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Channel [in]

The category of events to which this event belongs. The value is used to set the
**Channel** member of
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Level [in]

Specifies the severity of the event. The value is used to set the **Level**
member of
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Task [in]

Identifies a logical component of the application whose events you want to
enable. The value is used to set the **Task** member of
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Opcode [in]

Operation being performed at the time the event was written. The value is used
to set the **Opcode** member of
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Keyword [in]

Bitmask that further defines the category of events to which the event belongs.
The value is used to set the **Keyword** member of
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

## -returns

This function does not return a value.

## -remarks

This is a convenience macro for setting the members of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EventDescZero](/windows/desktop/api/evntprov/nf-evntprov-eventdesczero)

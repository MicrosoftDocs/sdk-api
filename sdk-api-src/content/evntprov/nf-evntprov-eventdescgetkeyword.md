---
UID: NF:evntprov.EventDescGetKeyword
title: EventDescGetKeyword function (evntprov.h)
description: Retrieves the keyword from the event descriptor.
helpviewer_keywords:
  [
    "EventDescGetKeyword",
    "EventDescGetKeyword function [ETW]",
    "base.eventdescgetkeyword_func",
    "etw.eventdescgetkeyword_func",
    "evntprov/EventDescGetKeyword",
  ]
old-location: etw\eventdescgetkeyword_func.htm
tech.root: ETW
ms.assetid: 4c96fad0-23c4-44cc-8b8f-2d62f08429d2
ms.date: 12/05/2018
ms.keywords:
  EventDescGetKeyword, EventDescGetKeyword function [ETW],
  base.eventdescgetkeyword_func, etw.eventdescgetkeyword_func,
  evntprov/EventDescGetKeyword
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
  - EventDescGetKeyword
  - evntprov/EventDescGetKeyword
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
  - EventDescGetKeyword
---

# EventDescGetKeyword function

## -description

Retrieves the keyword from the event descriptor.

## -parameters

### -param EventDescriptor [in]

Event descriptor from which to retrieve the keyword. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

## -returns

Keyword that is a bitmask that further defines the category of events to which
the event belongs.

## -remarks

This is a convenience macro for retrieving the member of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

---
UID: NF:evntprov.EventDescSetLevel
title: EventDescSetLevel function (evntprov.h)
description: Sets the Level member of the event descriptor.
helpviewer_keywords:
  [
    "EventDescSetLevel",
    "EventDescSetLevel function [ETW]",
    "base.eventdescsetlevel_func",
    "etw.eventdescsetlevel_func",
    "evntprov/EventDescSetLevel",
  ]
old-location: etw\eventdescsetlevel_func.htm
tech.root: ETW
ms.assetid: a4fe3b0e-6ca5-401c-a669-752e2955cc52
ms.date: 12/05/2018
ms.keywords:
  EventDescSetLevel, EventDescSetLevel function [ETW],
  base.eventdescsetlevel_func, etw.eventdescsetlevel_func,
  evntprov/EventDescSetLevel
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
  - EventDescSetLevel
  - evntprov/EventDescSetLevel
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
  - EventDescSetLevel
---

# EventDescSetLevel function

## -description

Sets the **Level** member of the event descriptor.

## -parameters

### -param EventDescriptor [in]

Event descriptor to modify. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Level [in]

Severity level that indicates the verboseness with which to log the event. For
details, see the Level parameter of
[EnableTraceEx](/windows/desktop/ETW/enabletraceex-func).

## -returns

The modified event descriptor.

## -remarks

This is a convenience macro for setting the member of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

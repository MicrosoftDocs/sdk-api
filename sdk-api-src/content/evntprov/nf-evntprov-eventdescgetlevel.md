---
UID: NF:evntprov.EventDescGetLevel
title: EventDescGetLevel function (evntprov.h)
description: Retrieves the severity level from the event descriptor.
helpviewer_keywords:
  [
    "EventDescGetLevel",
    "EventDescGetLevel function [ETW]",
    "base.eventdescgetlevel_func",
    "etw.eventdescgetlevel_func",
    "evntprov/EventDescGetLevel",
  ]
old-location: etw\eventdescgetlevel_func.htm
tech.root: ETW
ms.assetid: 29f356ad-c957-4a1e-abf8-5c7e6212c92e
ms.date: 12/05/2018
ms.keywords:
  EventDescGetLevel, EventDescGetLevel function [ETW],
  base.eventdescgetlevel_func, etw.eventdescgetlevel_func,
  evntprov/EventDescGetLevel
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
  - EventDescGetLevel
  - evntprov/EventDescGetLevel
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
  - EventDescGetLevel
---

# EventDescGetLevel function

## -description

Retrieves the severity level from the event descriptor.

## -parameters

### -param EventDescriptor [in]

Event descriptor from which to retrieve the severity level. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

## -returns

Severity level that indicates the verboseness with which to log the event.

## -remarks

This is a convenience macro for retrieving the member of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

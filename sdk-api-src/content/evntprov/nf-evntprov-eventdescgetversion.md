---
UID: NF:evntprov.EventDescGetVersion
title: EventDescGetVersion function (evntprov.h)
description: Retrieves the version from the event descriptor.
helpviewer_keywords:
  [
    "EventDescGetVersion",
    "EventDescGetVersion function [ETW]",
    "base.eventdescgetversion_func",
    "etw.eventdescgetversion_func",
    "evntprov/EventDescGetVersion",
  ]
old-location: etw\eventdescgetversion_func.htm
tech.root: ETW
ms.assetid: 3881f089-d0c6-4d46-929a-09777df13f61
ms.date: 12/05/2018
ms.keywords:
  EventDescGetVersion, EventDescGetVersion function [ETW],
  base.eventdescgetversion_func, etw.eventdescgetversion_func,
  evntprov/EventDescGetVersion
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
  - EventDescGetVersion
  - evntprov/EventDescGetVersion
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
  - EventDescGetVersion
---

# EventDescGetVersion function

## -description

Retrieves the version from the event descriptor.

## -parameters

### -param EventDescriptor [in]

Event descriptor from which to retrieve the version. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

## -returns

Version that identifies the revision level of the event definition.

## -remarks

This is a convenience macro for retrieving the member of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

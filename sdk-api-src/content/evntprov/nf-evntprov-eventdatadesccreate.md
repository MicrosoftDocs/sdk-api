---
UID: NF:evntprov.EventDataDescCreate
title: EventDataDescCreate function (evntprov.h)
description: Sets the values of an EVENT_DATA_DESCRIPTOR.
helpviewer_keywords:
  [
    "EventDataDescCreate",
    "EventDataDescCreate function [ETW]",
    "base.eventdatadesccreate_func",
    "etw.eventdatadesccreate_func",
    "evntprov/EventDataDescCreate",
  ]
old-location: etw\eventdatadesccreate_func.htm
tech.root: ETW
ms.assetid: a5823ad0-0710-4fd2-9b44-a60a42f138fd
ms.date: 12/05/2018
ms.keywords:
  EventDataDescCreate, EventDataDescCreate function [ETW],
  base.eventdatadesccreate_func, etw.eventdatadesccreate_func,
  evntprov/EventDataDescCreate
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
  - EventDataDescCreate
  - evntprov/EventDataDescCreate
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
  - EventDataDescCreate
---

# EventDataDescCreate function

## -description

Sets the values of an
[EVENT_DATA_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor).

## -parameters

### -param EventDataDescriptor [out]

The data descriptor whose member values are set to those of the remaining
parameters. For details, see
[EVENT_DATA_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor).

### -param DataPtr [in]

A pointer to the event data. This value is used to set the _Ptr_ member of the
descriptor.

_DataPtr_ parameter may be **NULL** if and only if _DataSize_ is 0.

### -param DataSize [in]

The size (in bytes) of the event data. The value is used to set the _Size_
member of the descriptor.

## -returns

This function does not return a value.

## -remarks

This is a convenience macro for setting the members of the
[EVENT_DATA_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
structure. Note that if you initialize the members yourself without calling
**EventDataDescCreate**, you should set `Ptr = (UINT_PTR)DataPtr`, and you
**must** initialize the _Reserved_ field (e.g. set it to 0),

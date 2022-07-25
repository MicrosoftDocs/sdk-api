---
UID: NF:evntprov.EventDescSetTask
title: EventDescSetTask function (evntprov.h)
description: Sets the Task member of the event descriptor.
helpviewer_keywords:
  [
    "EventDescSetTask",
    "EventDescSetTask function [ETW]",
    "base.eventdescsettask_func",
    "etw.eventdescsettask_func",
    "evntprov/EventDescSetTask",
  ]
old-location: etw\eventdescsettask_func.htm
tech.root: ETW
ms.assetid: 74298e6f-b29a-4fa7-98d1-f81270fcbc0e
ms.date: 12/05/2018
ms.keywords:
  EventDescSetTask, EventDescSetTask function [ETW], base.eventdescsettask_func,
  etw.eventdescsettask_func, evntprov/EventDescSetTask
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
  - EventDescSetTask
  - evntprov/EventDescSetTask
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
  - EventDescSetTask
---

# EventDescSetTask function

## -description

Sets the **Task** member of the event descriptor.

## -parameters

### -param EventDescriptor [in]

Event descriptor to modify. See
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor).

### -param Task [in]

Task that identifies the logical component of the application whose events you
want to enable.

## -returns

The modified event descriptor.

## -remarks

This is a convenience macro for setting the member of the
[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
structure.

## -see-also

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)

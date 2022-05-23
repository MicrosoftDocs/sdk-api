---
UID: NF:traceloggingprovider.TraceLoggingOpcode
title: TraceLoggingOpcode macro (traceloggingprovider.h)
description: Wrapper macro for setting the event's opcode.
helpviewer_keywords:
  [
    "TraceLoggingOpcode",
    "TraceLoggingOpcode macro",
    "tracelogging.traceloggingopcode",
    "traceloggingprovider/TraceLoggingOpcode",
  ]
old-location: tracelogging\traceloggingopcode.htm
tech.root: tracelogging
ms.assetid: 8D1459CE-51A8-49A8-A30B-EA8D87E822C3
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingOpcode, TraceLoggingOpcode macro, tracelogging.traceloggingopcode,
  traceloggingprovider/TraceLoggingOpcode
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2
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
  - TraceLoggingOpcode
  - traceloggingprovider/TraceLoggingOpcode
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingOpcode
---

# TraceLoggingOpcode macro

## -description

Wrapper macro for setting the event's opcode.

## -parameters

### -param eventOpcode [in]

The event opcode. The event opcode must be a compile-time constant between 0
and 255.

## -remarks

If TraceLoggingOpcode has no provided argument, the default opcode is 0
(EVENT_TRACE_TYPE_INFO). If multiple arguments are provided, the value from the
previous call to TraceLoggingOpcode is used.

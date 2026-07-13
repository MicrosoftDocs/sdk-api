---
UID: NF:traceloggingprovider.TraceLoggingDescription
title: TraceLoggingDescription macro (traceloggingprovider.h)
description: TraceLogging wrapper macro that sets the description for the event.
helpviewer_keywords:
  [
    "TraceLoggingDescription",
    "TraceLoggingDescription macro",
    "tracelogging.traceloggingdescription",
    "traceloggingprovider/TraceLoggingDescription",
  ]
old-location: tracelogging\traceloggingdescription.htm
tech.root: tracelogging
ms.assetid: 90521B97-2651-46C9-8292-925F53F88CE7
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingDescription, TraceLoggingDescription macro,
  tracelogging.traceloggingdescription,
  traceloggingprovider/TraceLoggingDescription
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
  - TraceLoggingDescription
  - traceloggingprovider/TraceLoggingDescription
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
  - TraceLoggingDescription
---

# TraceLoggingDescription macro

## -syntax

```cpp
void TraceLoggingDescription(
  [in]  string eventDescription
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that sets the description for the event.

## -parameters

### -param eventDescription [in]

The description of the event. This value must be a string literal.

## -remarks

`TraceLoggingDescription("event description")` can be used as a parameter to an
invocation of a
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro.

If multiple description args are provided, they are concatenated together into a
single string.

Event descriptions are stored in the
[PDB](/windows-hardware/drivers/debugger/symbols). They are not available at
runtime.

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

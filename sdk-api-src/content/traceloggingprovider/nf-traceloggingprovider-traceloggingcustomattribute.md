---
UID: NF:traceloggingprovider.TraceLoggingCustomAttribute
title: TraceLoggingCustomAttribute macro (traceloggingprovider.h)
description:
  TraceLogging wrapper macro that adds custom information about the event into
  the PDB.
helpviewer_keywords:
  [
    "TraceLoggingCustomAttribute",
    "TraceLoggingCustomAttribute macro",
    "tracelogging.traceloggingcustomattribute",
    "traceloggingprovider/TraceLoggingCustomAttribute",
  ]
old-location: tracelogging\traceloggingcustomattribute.htm
tech.root: tracelogging
ms.assetid: D58950A3-105D-43C7-8B8B-61CC1F0D4DA0
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingCustomAttribute, TraceLoggingCustomAttribute macro,
  tracelogging.traceloggingcustomattribute,
  traceloggingprovider/TraceLoggingCustomAttribute
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
  - TraceLoggingCustomAttribute
  - traceloggingprovider/TraceLoggingCustomAttribute
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
  - TraceLoggingCustomAttribute
---

# TraceLoggingCustomAttribute macro

## -syntax

```cpp
void TraceLoggingCustomAttribute(
  [in]  string key,
  [in]  string value
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that adds custom information about the event into the PDB.

## -parameters

### -param key [in]

A string literal with the key for the custom attribute.

### -param value [in]

A string literal with the value of the custom attribute.

## -remarks

`TraceLoggingCustomAttribute("key", "value")` can be used as a parameter to an
invocation of a
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro. Most
TraceLogging events do not need custom attributes and should not use
TraceLoggingCustomAttribute.

Custom attributes are stored in the
[PDB](/windows-hardware/drivers/debugger/symbols). They are not available at
runtime.

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

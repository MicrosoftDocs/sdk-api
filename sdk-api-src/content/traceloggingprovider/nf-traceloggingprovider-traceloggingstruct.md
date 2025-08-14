---
UID: NF:traceloggingprovider.TraceLoggingStruct
title: TraceLoggingStruct macro (traceloggingprovider.h)
description:
  TraceLogging wrapper macro that adds a field that contains other fields to the
  event.
helpviewer_keywords:
  [
    "TraceLoggingStruct",
    "TraceLoggingStruct macro",
    "tracelogging.traceloggingstruct",
    "traceloggingprovider/TraceLoggingStruct",
  ]
old-location: tracelogging\traceloggingstruct.htm
tech.root: tracelogging
ms.assetid: 9F681D04-98DF-4B27-9A40-740B2F0B287D
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingStruct, TraceLoggingStruct macro, tracelogging.traceloggingstruct,
  traceloggingprovider/TraceLoggingStruct
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
  - TraceLoggingStruct
  - traceloggingprovider/TraceLoggingStruct
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
  - TraceLoggingStruct
---

# TraceLoggingStruct macro

## -syntax

```cpp
void TraceLoggingStruct(
  [in]            int fieldCount,
  [in]            string name,
  [in, optional]  string description,
  [in, optional]  int tags
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that adds a field that contains other fields to the event.

## -parameters

### -param fieldCount [in]

The number of fields that will be considered part of the structure. This
parameter must be a compile-time constant.

### -param name [in]

The name to use for the structure in the event. The name parameter must be a
string literal (not a variable) and must not contain any '\0' characters.

### -param __VA_ARGS__ [in, optional]

Optional _description_ and _tags_ parameters for the field definition.

TraceLoggingStruct can be specified with 2, 3, or 4 parameters. If a parameter
is not specified, a default will be used. For example,
`TraceLoggingStruct(3, "MyStruct")` is equivalent to
`TraceLoggingStruct(3, "MyStruct", "", 0)`.

- `[in, optional] description`

  The description of the event field's value. If provided, the description
  parameter must be a string literal and will be included in the
  [PDB](/windows-hardware/drivers/debugger/symbols).

- `[in, optional] tags`

  A compile-time constant integer value. The low 28 bits of the value will be
  included in the field's metadata. The semantics of this value are defined by
  the event consumer. During event processing, this value can be retrieved from
  the [EVENT_PROPERTY_INFO](../tdh/ns-tdh-event_property_info.md) Tags field.

## -remarks

`TraceLoggingStruct(fieldCount, name, ...)` can be used as a parameter to an
invocation of a
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro. Each
TraceLoggingStruct parameter adds one logical field to the event. The field is a
structure or group that contains the subsequent _fieldCount_ logical fields as
its value.

### Examples

```c
TraceLoggingWrite(
    g_hProvider,
    "MyEventWithStruct",
    TraceLoggingLevel(WINEVENT_LEVEL_WARNING), // Levels defined in <winmeta.h>
    TraceLoggingKeyword(MyEventCategories), // Provider-defined categories
    TraceLoggingInt32(num1, "BeforeStruct"),
    TraceLoggingStruct(3, "StructWith3Fields"),
        TraceLoggingInt32(num2, "StructField1"),
        TraceLoggingInt32(num3, "StructField2"),
        TraceLoggingInt32(num4, "StructField3"),
    TraceLoggingInt32(num5, "AfterStruct));

TraceLoggingWrite(
    g_hProvider,
    "MyEventWithNestedStruct",
    TraceLoggingLevel(WINEVENT_LEVEL_VERBOSE), // Levels defined in <winmeta.h>
    TraceLoggingKeyword(MyEventCategories), // Provider-defined categories
    TraceLoggingInt32(num1, "BeforeStruct"),
    TraceLoggingStruct(3, "StructWith3Fields"),
        TraceLoggingInt32(num2, "StructField1"),
        TraceLoggingStruct(2, "StructField2"),
            TraceLoggingInt32(num3, "StructField2NestedField1"),
            TraceLoggingInt32(num4, "StructField2NestedField2"),
        TraceLoggingInt32(num5, "StructField3"),
    TraceLoggingInt32(num6, "AfterStruct));
```

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

---
UID: NF:traceloggingprovider.TraceLoggingCustom
title: TraceLoggingCustom macro (traceloggingprovider.h)
description:
  TraceLogging wrapper macro that adds a field that was packed using a custom
  serializer to the event.
helpviewer_keywords:
  [
    "TraceLoggingCustom",
    "TraceLoggingCustom macro",
    "tracelogging.traceloggingcustom",
    "traceloggingprovider/TraceLoggingCustom",
  ]
old-location: tracelogging\traceloggingcustom.htm
tech.root: tracelogging
ms.assetid: 617B5EFF-DB4F-493E-841B-14BBA312E26B
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingCustom, TraceLoggingCustom macro, tracelogging.traceloggingcustom,
  traceloggingprovider/TraceLoggingCustom
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
  - TraceLoggingCustom
  - traceloggingprovider/TraceLoggingCustom
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
  - TraceLoggingCustom
---

# TraceLoggingCustom macro

## -syntax

```cpp
void TraceLoggingCustom(
  [in]             pValue,
  [in]             cbValue,
  [in]             protocol,
  [in]             bSchema,
  [in]             cbSchema,
  [in, optional]   name,
  [in, optional]   description,
  [in, optional]   tags
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that adds a field that was packed using a custom serializer to the event.

Most TraceLogging events do not need to use a custom serializer and should not
use TraceLoggingCustom.

## -parameters

### -param pValue [in]

A pointer to the field's payload, serialized at runtime by a serializer from the
specified protocol family.

### -param cbValue [in]

The size, in bytes, of the field's payload, serialized at runtime by a
serializer from the specified protocol family.

### -param protocol [in]

A protocol family, which may be a Microsoft-defined value from 0-4 or a
user-defined value from 5-31. The Microsoft-defined values are defined by macros
starting with `TRACELOGGING_PROTOCOL_`.

### -param bSchema [in]

A comma-separated list of byte values that contain the information needed to
decode the payload (i.e. the schema), in a protocol-defined format. The values
in this list must be compile-time constant. Example: (0x12, 0x23, 0x34)

### -param cbSchema [in]

The number of byte values provided in _bSchema_. This value must be a
compile-time constant.

### -param __VA_ARGS__ [in, optional]

Optional _name_, _description_, and _tags_ parameters for the field definition.

TraceLoggingCustom can be specified with 5, 6, 7, or 8 parameters. If a
parameter is not specified, a default will be used. For example,
`TraceLoggingCustom(&x.data, sizeof(x.data), p, (schema), cbSchema)` is
equivalent to
`TraceLoggingCustom(&x.data, sizeof(x.data), p, (schema), cbSchema, "&x.data", "", 0)`.

- `[in, optional] name`

  The name to use for the event field. If provided, the name parameter must be a
  string literal (not a variable) and must not contain any '\0' characters. If
  not provided, the event field name will be based on _pValue_.

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

`TraceLoggingCustom(pValue, cbValue, protocol, (schema...), cbSchema, ...)` can
be used as a parameter to an invocation of a
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro. Each
TraceLoggingCustom parameter adds a custom-serialized field to the event. Most
TraceLogging events do not use custom serializers and should not use
TraceLoggingCustom. General-purpose ETW decoders do not support fields that use
custom serialization and will typically treat the fields as TDH_INTYPE_BINARY.

Decoders should access TraceLoggingCustom serialized fields using the TDH APIs.
The TRACE_EVENT_INFO structure returned by TdhGetEventInformation will contain
two EVENT_PROPERTY_INFO structures related to a logged TraceLoggingCustom field.
These correlate in the typical fashion with the data found in the EVENT_RECORD's
UserData blob for a binary field (TDH_INTYPE_BINARY).

- The first of the two EVENT_PROPERTY_INFO structures is the "Length" property
  which describes the length of the serialized payload (i.e. cbValue).
- The second is the property that refers to the user's payload (pbValue). The
  second property will have PropertyParamLength (in reference to the "Length"
  property) and PropertyHasCustomSchema set.

Decoders should recognize that PropertyHasCustomSchema has been set and consult
the EVENT_PROPERTY_INFO's customSchemaType member for the CustomSchemaOffset,
which is the offset in the TRACE_EVENT_INFORMATION where the protocol type and
protocol metadata are located. There, they can find the metadata they passed in
with a format of (pseudo-struct):

```c
struct _CUSTOM_SCHEMA {
    UINT16 protocolType;
    UINT16 cbSchema;
    BYTE bSchema[cbSchema];
};
```

Existing decoders that do not take these extra steps to recognize the
PropertyHasCustomSchema flag and instead refer to the nonStructType part of the
EVENT_PROPERTY_INFO union to decode the event will seamlessly treat the payload
as if it were TDH_INTYPE_BINARY.

### Examples

```cpp
// Value generated at runtime by serializer:
BYTE rgValue[] = {...};

TraceLoggingWrite(
   g_hProvider,
   "MyEventName",
   TraceLoggingCustom(
      rgValue,
      sizeof(rgValue),
      TRACELOGGING_PROTOCOL_MYPROTOCOL,
      ( 0x0, 0x1, 0x2 ), // Generated at compile-time
      3,
      "MyCustomField"),
   TraceLoggingLevel(WINEVENT_LEVEL_WARNING), // Levels defined in <winmeta.h>
   TraceLoggingKeyword(MyEventCategories)); // Provider-defined categories
```

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

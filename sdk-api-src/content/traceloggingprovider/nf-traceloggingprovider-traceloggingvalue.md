---
UID: NF:traceloggingprovider.TraceLoggingValue
title: TraceLoggingValue macro (traceloggingprovider.h)
description:
  TraceLogging wrapper macro for C++ that adds a field with an
  automatically-deduced type to the event.
helpviewer_keywords:
  [
    "TraceLoggingValue",
    "TraceLoggingValue macro",
    "tracelogging.traceloggingvalue",
    "traceloggingprovider/TraceLoggingValue",
  ]
old-location: tracelogging\traceloggingvalue.htm
tech.root: tracelogging
ms.assetid: F4013632-3DC8-413C-B25F-64DE070FA4A8
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingValue, TraceLoggingValue macro, tracelogging.traceloggingvalue,
  traceloggingprovider/TraceLoggingValue
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
  - TraceLoggingValue
  - traceloggingprovider/TraceLoggingValue
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
  - TraceLoggingValue
---

# TraceLoggingValue macro

## -syntax

```cpp
void TraceLoggingValue(
  [in]             value,
  [in, optional]  UINT name,
  [in, optional]  UINT description,
  [in, optional]  int tags
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
for C++ that adds a field with an automatically-deduced type to the event.

## -parameters

### -param value [in]

The event field value.

### -param __VA_ARGS__ [in, optional]

Optional _name_, _description_, and _tags_ parameters for the field definition.

TraceLoggingValue can be specified with 1, 2, 3, or 4 parameters. If a parameter
is not specified, a default will be used. For example, `TraceLoggingValue(a+b)`
is equivalent to `TraceLoggingValue(a+b, "a+b", "", 0)`.

- `[in, optional] name`

  The name to use for the event field. If provided, the name parameter must be a
  string literal (not a variable) and must not contain any '\0' characters. If
  not provided, the event field name will be based on _value_.

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

In C++ code, `TraceLoggingValue(value, ...)` can be used as a parameter to an
invocation of a
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro. Each
TraceLoggingValue parameter adds one field to the event.

The type of the field in the ETW event is automatically deduced from the type of
the _value_ expression. Based on the type of _value_,
`TraceLoggingValue(value, ...)` is equivalent to one of the standard
TraceLogging wrapper macros as follows:

| Type of _value_ | Equivalent to          | Notes                                                    |
| --------------- | ---------------------- | -------------------------------------------------------- |
| `bool`          | TraceLoggingBoolean    |
| `char`          | TraceLoggingChar       | Only for char, not for signed char or unsigned char.     |
| `char16_t`      | TraceLoggingChar16     |
| `wchar_t`       | TraceLoggingWChar      | Only for native wchar_t, not for USHORT.                 |
| `intNN_t`       | TraceLoggingIntNN      | For signed char, short, int, long, and long long.        |
| `uintNN_t`      | TraceLoggingUIntNN     | For unsigned char, short, int, long, and long long.      |
| `float`         | TraceLoggingFloat32    |
| `double`        | TraceLoggingFloat64    |
| `GUID`          | TraceLoggingGuid       |
| `FILETIME`      | TraceLoggingFileTime   |
| `SYSTEMTIME`    | TraceLoggingSystemTime |
| `SID*`          | TraceLoggingSid        | Must be non-NULL and must point to a valid `SID`.        |
| `void*`         | TraceLoggingPointer    | Logs the pointer value, not the referenced data.         |
| `char*`         | TraceLoggingString     | Zero-terminated CP_ACP string. NULL is treated as `""`.  |
| `char16_t*`     | TraceLoggingString16   | Zero-terminated UTF-16 string. NULL is treated as `u""`. |
| `wchar_t*`      | TraceLoggingWideString | Zero-terminated UTF-16 string. NULL is treated as `L""`. |

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

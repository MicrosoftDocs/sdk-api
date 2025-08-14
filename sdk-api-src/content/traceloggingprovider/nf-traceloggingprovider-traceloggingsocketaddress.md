---
UID: NF:traceloggingprovider.TraceLoggingSocketAddress
title: TraceLoggingSocketAddress macro (traceloggingprovider.h)
description:
  TraceLogging wrapper macro that adds a field with a socket address to the
  event.
helpviewer_keywords:
  [
    "TraceLoggingSocketAddress",
    "TraceLoggingSocketAddress macro",
    "tracelogging.traceloggingsocketaddress",
    "traceloggingprovider/TraceLoggingSocketAddress",
  ]
old-location: tracelogging\traceloggingsocketaddress.htm
tech.root: tracelogging
ms.assetid: 7965C10A-2C19-4AA3-A9E3-7219EFB2D3A0
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingSocketAddress, TraceLoggingSocketAddress macro,
  tracelogging.traceloggingsocketaddress,
  traceloggingprovider/TraceLoggingSocketAddress
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
  - TraceLoggingSocketAddress
  - traceloggingprovider/TraceLoggingSocketAddress
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
  - TraceLoggingSocketAddress
---

# TraceLoggingSocketAddress macro

## -syntax

```cpp
void TraceLoggingSocketAddress(
  [in]            SOCKADDR* pValue,
  [in]            byte cbValue,
  [in, optional]  String name,
  [in, optional]  String description,
  [in, optional]  Integer tags
);
```

## -description

[TraceLogging wrapper macro](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
that adds a field with a socket address to the event.

## -parameters

### -param pValue [in]

A pointer to a sockaddr structure.

### -param cbValue [in]

The size, in bytes, of the value pointed to by the _pValue_ parameter.

> [!NOTE]
> The amount of data needed for a sockaddr field varies depending on the
> type of address. If the data is stored in a union variable, be sure to set the
> cbValue parameter to the size of the correct union member (or to the size of
> the union) to avoid truncating the data.

### -param __VA_ARGS__ [in, optional]

Optional _name_, _description_, and _tags_ parameters for the field definition.

TraceLoggingSocketAddress can be specified with 2, 3, 4, or 5 parameters. If a
parameter is not specified, a default will be used. For example,
`TraceLoggingSocketAddress(&x.sockAddr, sizeof(x.sockAddr))` is equivalent to
`TraceLoggingSocketAddress(&x.sockAddr, sizeof(x.sockAddr), "&x.sockAddr", "", 0)`.

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

`TraceLoggingSocketAddress(pValue, cbValue, ...)` can be used as a parameter to
an invocation of a
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro. Each
TraceLoggingSocketAddress parameter adds one field to the event.

The value may be any Windows sockaddr type, e.g.
[SOCKADDR](../ws2def/ns-ws2def-sockaddr.md),
[SOCKADDR_IN](../ws2def/ns-ws2def-sockaddr_in.md),
[SOCKADDR_IN6](../ws2ipdef/ns-ws2ipdef-sockaddr_in6_lh.md),
[SOCKADDR_STORAGE](../ws2def/ns-ws2def-sockaddr_storage_lh.md), etc. The event
will record the raw binary data and the data size. The event decoder will use
the `sa_family` field to determine the actual type of the socket address.

> [!NOTE]
> Not all decoders will support all sockaddr family types. If an
> unsupported sockaddr is encountered, the decoder might decode the field as raw
> binary data instead of formatting it as an address.

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

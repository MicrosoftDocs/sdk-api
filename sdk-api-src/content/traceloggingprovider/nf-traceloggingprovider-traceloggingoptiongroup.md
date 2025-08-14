---
UID: NF:traceloggingprovider.TraceLoggingOptionGroup
title: TraceLoggingOptionGroup macro (traceloggingprovider.h)
description:
  TraceLogging macro for use in TRACELOGGING_DEFINE_PROVIDER to specify a
  provider group.
helpviewer_keywords:
  [
    "TraceLoggingOptionGroup",
    "TraceLoggingOptionGroup macro",
    "tracelogging.traceloggingoptiongroup",
    "traceloggingprovider/TraceLoggingOptionGroup",
  ]
old-location: tracelogging\traceloggingoptiongroup.htm
tech.root: tracelogging
ms.assetid: 5D794C46-95B2-4111-AFB8-CE488B4D1A42
ms.date: 07/01/2025
ms.keywords:
  TraceLoggingOptionGroup, TraceLoggingOptionGroup macro,
  tracelogging.traceloggingoptiongroup,
  traceloggingprovider/TraceLoggingOptionGroup
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
  - TraceLoggingOptionGroup
  - traceloggingprovider/TraceLoggingOptionGroup
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
  - TraceLoggingOptionGroup
---

# TraceLoggingOptionGroup macro

## -syntax

```cpp
void TraceLoggingOptionGroup(
  [in]  UINT32 g1,
  [in]   g2,
  [in]   g3,
  [in]   g4,
  [in]   g5,
  [in]   g6,
  [in]   g7,
  [in]   g8,
  [in]   g9,
  [in]   g10,
  [in]   g11
);
```

## -description

TraceLogging macro for use in
[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)
to specify a provider group.

Most TraceLogging providers are not associated with a provider group and do not
need to use TraceLoggingOptionGroup.

## -parameters

### -param g1 [in]

The first 4 bytes of the GUID.

### -param g2 [in]

The next 2 bytes of the GUID.

### -param g3 [in]

The next 2 bytes of the GUID.

### -param g4 [in]

The next byte of the GUID.

### -param g5 [in]

The next byte of the GUID.

### -param g6 [in]

The next byte of the GUID.

### -param g7 [in]

The next byte of the GUID.

### -param g8 [in]

The next byte of the GUID.

### -param g9 [in]

The next byte of the GUID.

### -param g10 [in]

The next byte of the GUID.

### -param g11 [in]

The next byte of the GUID.

## -remarks

If you want your provider to be associated with an
[ETW provider group](/windows/win32/etw/provider-traits), add the
[TraceLoggingOptionGroup](./nf-traceloggingprovider-traceloggingoptiongroup.md)
macro to the
[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)
declaration to specify the provider's group GUID.

A provider can be a member of no more than one group. The semantics of group
membership are determined by ETW controllers that subscribe a session to a group
via [EnableTraceEx2](../evntrace/nf-evntrace-enabletraceex2.md) with
EVENT_ENABLE_PROPERTY_PROVIDER_GROUP.

### Examples

```c
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyProvider,
    "MyProvider",
    // {b3864c38-4273-58c5-545b-8b3608343471}
    (0xb3864c38,0x4273,0x58c5,0x54,0x5b,0x8b,0x36,0x08,0x34,0x34,0x71),
    // {798d0c76-4209-5932-a2af-2d94a2e66c45}
    TraceLoggingOptionGroup(0x798d0c76,0x4209,0x5932,0xa2,0xaf,0x2d,0x94,0xa2,0xe6,0x6c,0x45));
```

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

[EnableTraceEx2](../evntrace/nf-evntrace-enabletraceex2.md)

[Provider Traits](/windows/win32/etw/provider-traits)

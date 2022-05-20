---
UID: NF:traceloggingprovider.TraceLoggingOptionGroup
title: TraceLoggingOptionGroup macro (traceloggingprovider.h)
description:
  Wrapper macro for use in TRACELOGGING_DEFINE_PROVIDER to declare the GUID of
  the provider group that the provider is a member of.
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
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingOptionGroup, TraceLoggingOptionGroup macro,
  tracelogging.traceloggingoptiongroup,
  traceloggingprovider/TraceLoggingOptionGroup
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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

## -description

Wrapper macro for use in
[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)
to declare the GUID of the provider group that the provider is a member of.

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

A provider can be a member of no more than one group. The semantics of group
membership are determined by ETW controllers that subscribe a session to a
group.

The following code sample shows how to construct the GUID:

```c
TraceLoggingOptionGroup(0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33);
```

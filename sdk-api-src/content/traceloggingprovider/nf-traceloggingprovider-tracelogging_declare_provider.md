---
UID: NF:traceloggingprovider.TRACELOGGING_DECLARE_PROVIDER
title: TRACELOGGING_DECLARE_PROVIDER macro (traceloggingprovider.h)
description: Forward-declares a handle for a TraceLogging provider.
helpviewer_keywords:
  [
    "TRACELOGGING_DECLARE_PROVIDER",
    "TRACELOGGING_DECLARE_PROVIDER macro",
    "tracelogging.TRACELOGGING_DECLARE_PROVIDER",
    "tracelogging.traceloggingdeclareprovider",
    "traceloggingprovider/TRACELOGGING_DECLARE_PROVIDER",
  ]
old-location: tracelogging\TRACELOGGING_DECLARE_PROVIDER.htm
tech.root: tracelogging
ms.assetid: E9C0B622-77A5-498F-BB28-C6C181271276
ms.date: 06/06/2022
ms.keywords:
  TRACELOGGING_DECLARE_PROVIDER, TRACELOGGING_DECLARE_PROVIDER macro,
  tracelogging.TRACELOGGING_DECLARE_PROVIDER,
  tracelogging.traceloggingdeclareprovider,
  traceloggingprovider/TRACELOGGING_DECLARE_PROVIDER
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
  - TRACELOGGING_DECLARE_PROVIDER
  - traceloggingprovider/TRACELOGGING_DECLARE_PROVIDER
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
  - TRACELOGGING_DECLARE_PROVIDER
---

# TRACELOGGING_DECLARE_PROVIDER macro

## -description

Forward-declares a handle for a TraceLogging provider.

## -parameters

### -param handleVariable [in]

The handle name to forward-declare. This should be the name of a handle that has
been defined in a .c or .cpp file using
[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md).

## -remarks

Use this macro as needed to forward-declare your TraceLogging provider handle,
e.g. in a header file of your component. This macro does not allocate storage
for the provider handle. In order to use the provider, you will need to use
[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)
to define the handle and
[TraceLoggingRegister](./nf-traceloggingprovider-traceloggingregister.md) to
register it.

An invocation like `TRACELOGGING_DECLARE_PROVIDER(MyProviderHandle)` can be
thought of as similar to code like:

```c
extern "C" const TraceLoggingHProvider MyProviderHandle;
```

> [!NOTE]
> The provider handle declared by `TRACELOGGING_DECLARE_PROVIDER` has
> module scope. It can be used as needed within the EXE, DLL, or SYS file but
> should not be shared with other DLLs in the same process. Each EXE, DLL, or
> SYS file should define its own provider handle and should perform its own
> Register and Unregister.

## -see-also

[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

---
UID: NF:traceloggingprovider.TRACELOGGING_DECLARE_PROVIDER
title: TRACELOGGING_DECLARE_PROVIDER macro (traceloggingprovider.h)
description: Forward declares a global TraceLogging provider handle.
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
ms.date: 12/05/2018
ms.keywords:
  TRACELOGGING_DECLARE_PROVIDER, TRACELOGGING_DECLARE_PROVIDER macro,
  tracelogging.TRACELOGGING_DECLARE_PROVIDER,
  tracelogging.traceloggingdeclareprovider,
  traceloggingprovider/TRACELOGGING_DECLARE_PROVIDER
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

Forward declares a global TraceLogging provider handle.

## -parameters

### -param handleVariable [in]

The handle variable name to forward declare.

## -remarks

Use this macro in a shared header file to forward declare your TraceLogging
provider handle. This macro does not allocate storage for the provider. In order
to use the provider, you will need to use
[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)
to define the variable.

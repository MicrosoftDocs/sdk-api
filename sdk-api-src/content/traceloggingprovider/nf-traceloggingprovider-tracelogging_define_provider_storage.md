---
UID: NF:traceloggingprovider.TRACELOGGING_DEFINE_PROVIDER_STORAGE
title: TRACELOGGING_DEFINE_PROVIDER_STORAGE macro (traceloggingprovider.h)
description:
  Allocates storage for a TraceLogging provider. This macro should only be used
  for advanced scenarios.
helpviewer_keywords:
  [
    "TRACELOGGING_DEFINE_PROVIDER_STORAGE",
    "TRACELOGGING_DEFINE_PROVIDER_STORAGE macro",
    "tracelogging.TRACELOGGING_DEFINE_PROVIDER_STORAGE",
    "tracelogging.traceloggingproviderstorage",
    "traceloggingprovider/TRACELOGGING_DEFINE_PROVIDER_STORAGE",
  ]
old-location: tracelogging\TRACELOGGING_DEFINE_PROVIDER_STORAGE.htm
tech.root: tracelogging
ms.assetid: C7244C95-5F02-4336-ADFF-876514665C87
ms.date: 12/05/2018
ms.keywords:
  TRACELOGGING_DEFINE_PROVIDER_STORAGE, TRACELOGGING_DEFINE_PROVIDER_STORAGE
  macro, tracelogging.TRACELOGGING_DEFINE_PROVIDER_STORAGE,
  tracelogging.traceloggingproviderstorage,
  traceloggingprovider/TRACELOGGING_DEFINE_PROVIDER_STORAGE
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
  - TRACELOGGING_DEFINE_PROVIDER_STORAGE
  - traceloggingprovider/TRACELOGGING_DEFINE_PROVIDER_STORAGE
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
  - TRACELOGGING_DEFINE_PROVIDER_STORAGE
---

# TRACELOGGING_DEFINE_PROVIDER_STORAGE macro

## -description

Allocates storage for a TraceLogging provider. This macro should only be used
for advanced scenarios.

## -parameters

### -param storageVariable [in]

A handle to the data storage allocated for the TraceLogging provider.

### -param providerName [in]

The name of the TraceLogging provider. This must be a string literal and cannot
be a variable.

### -param providerId [in]

The GUID for the provider.

#### - options [in, optional]

The GUID of the provider group that your provider is a member of.

## -remarks

Use this macro to allocate storage but not define a handle for the TraceLogging
provider. This is useful for scenarios where you need to have greater control
over the way that your app manages registration for global handles.

Use the
[TraceLoggingOptionGroup](./nf-traceloggingprovider-traceloggingoptiongroup.md)
macro to specify the GUID of the provider group that the provider belongs to. A
provider can be a member of no more than one group. The semantics of group
membership are determined by the ETW controllers that subscribe a session to a
group.

**TRACELOGGING_DEFINE_PROVIDER_STORAGE** will declare a static variable with the
data needed for a provider. You can then create a handle by taking the address
of this variable. Example usage:

```c
TRACELOGGING_DEFINE_PROVIDER_STORAGE(s_myProvider, "MyProvider", (...GUID...));
const TraceLoggingHProvider g_hMyProvider = &s_myProvider;
```

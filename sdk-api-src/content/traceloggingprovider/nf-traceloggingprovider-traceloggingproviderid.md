---
UID: NF:traceloggingprovider.TraceLoggingProviderId
title: TraceLoggingProviderId
description: Gets the provider ID of a TraceLogging provider.
ms.date: 06/06/2022
ms.keywords: TraceLoggingProviderId
targetos: Windows
req.assembly:
req.construct-type: function
req.ddi-compliance:
req.dll:
req.header: traceloggingprovider.h
req.idl:
req.include-header:
req.irql:
req.kmdf-ver:
req.lib:
req.max-support:
req.namespace:
req.redist:
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.target-type:
req.type-library:
req.umdf-ver:
req.unicode-ansi:
f1_keywords:
  - TraceLoggingProviderId
  - traceloggingprovider/TraceLoggingProviderId
dev_langs:
  - c++
topic_type:
  - apiref
api_type:
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingProviderId
---

## -description

Gets the provider ID of a TraceLogging provider.

## -parameters

### -param hProvider

The handle of the TraceLogging provider for which the provider ID is needed.

## -returns

The provider ID (GUID) that was specified in the
[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)
that defined the specified handle.

## -see-also

[TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)

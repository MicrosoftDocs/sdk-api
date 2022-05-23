---
UID: NF:traceloggingprovider.TraceLoggingProviderEnabled
title: TraceLoggingProviderEnabled
ms.date: 5/7/2019
ms.keywords: TraceLoggingProviderEnabled
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type:
req.type-library:
req.umdf-ver:
req.unicode-ansi:
f1_keywords:
  - TraceLoggingProviderEnabled
  - traceloggingprovider/TraceLoggingProviderEnabled
dev_langs:
  - c++
topic_type:
  - apiref
api_type:
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingProviderEnabled
---

## -description

Indicates whether any sessions have subscribed to the provider.

## -parameters

### -param hProvider

The handle to the provider to check.

### -param eventLevel

The event level that you want to check. An event level of 0 indicates any
events.

### -param eventKeyword

The keyword that you want to check. A keyword of 0 indicates no specific
keywords.

## -returns

Returns **TRUE** if any session has subscribed to the handler matching the event
criteria; **FALSE** otherwise.

## -remarks

## -see-also

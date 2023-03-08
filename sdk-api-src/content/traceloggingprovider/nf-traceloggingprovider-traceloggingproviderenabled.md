---
UID: NF:traceloggingprovider.TraceLoggingProviderEnabled
title: TraceLoggingProviderEnabled
description:
  TraceLogging macro to determine whether a any trace consumer is listening for
  an event from this provider.
ms.date: 06/06/2022
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
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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

TraceLogging macro to determine whether a any trace consumer is listening for an
event from this provider.

## -parameters

### -param hProvider

The handle to the TraceLogging provider to check.

### -param eventLevel

The event level that you want to check. An event level of 0 indicates any
events.

### -param eventKeyword

The keyword that you want to check. A keyword of 0 indicates no specific
keywords.

## -returns

Returns **TRUE** if any trace consumer session is listening to events matching
the specified criteria, **FALSE** otherwise.

## -remarks

This API provides a simple way to determine whether an event is enabled, i.e.
whether any event consumer sessions would be interested in receiving an event
from the specified provider with the specified level and keyword.

> [!NOTE]
> This API performs a conservative quick test. It is possible for this
> API to return true in certain cases where subsequent in-depth filtering would
> determine that no sessions actually need to record the event.

Most event providers will not call **TraceLoggingProviderEnabled** directly. The
[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md) macro
performs its own TraceLoggingProviderEnabled test and returns immediately if the
event is not enabled. However, it may be useful for a provider to call
**TraceLoggingProviderEnabled** before performing complex preparations before
invoking a **TraceLoggingWrite** macro.

### Examples

```cpp
// Skip GetMyInformation() if nobody is listening for MyInformationEvent:
if (TraceLoggingProviderEnabled(MyProvider, MyEventLevel, MyEventKeyword))
{
    MY_INFORMATION info;
    GetMyInformation(&info);

    TraceLoggingWrite(
        MyProvider,
        "MyInformationEvent",
        TraceLoggingLevel(MyEventLevel),
        TraceLoggingKeyword(MyEventKeyword),
        TraceLoggingValue(info.Val1),
        TraceLoggingValue(info.Val2));
}
```

## -see-also

[TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)

[TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)

[EventProviderEnabled](../evntprov/nf-evntprov-eventproviderenabled.md)

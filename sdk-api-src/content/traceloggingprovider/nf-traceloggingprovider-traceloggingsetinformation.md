---
UID: NF:traceloggingprovider.TraceLoggingSetInformation
title: TraceLoggingSetInformation
ms.date: 5/7/2019
ms.keywords: TraceLoggingSetInformation
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
  - TraceLoggingSetInformation
  - traceloggingprovider/TraceLoggingSetInformation
dev_langs:
  - c++
topic_type:
  - apiref
api_type:
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingSetInformation
---

## -description

Provides special-purpose information to the Event Tracing for Windows (ETW)
runtime.

## -parameters

### -param hProvider

Handle to the provider.

### -param informationClass

The type of information for the provider.

### -param pvInformation

The input buffer.

### -param cbInformation

The size of the input buffer.

## -returns

If you call this function from user mode code, the function returns a HRESULT.
Use the SUCCEEDED() macro to determine if the function succeeds.

If you call this function from kernel mode code, the function returns a
NTSTATUS. Use the NT_SUCCESS() macro to determine if the function succeeds.

## -remarks

This function serves as a wrapper around the
[EventSetInformation](../evntprov/nf-evntprov-eventsetinformation.md) function.

To control the behavior of this function, use macros `TLG_EVENT_SET_INFORMATION`
and `TLG_HAVE_EVENT_SET_INFORMATION`.

## -see-also

---
UID: NF:traceloggingprovider.TraceLoggingSetInformation
title: TraceLoggingSetInformation
description: Configures a TraceLogging provider by calling EventSetInformation.
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

Configures a TraceLogging provider by calling
[EventSetInformation](../evntprov/nf-evntprov-eventsetinformation.md).

## -parameters

### -param hProvider

Handle to the TraceLogging provider to be configured. The provider must be in
the [registered](./nf-traceloggingprovider-traceloggingregister.md) state.

### -param informationClass

The [EVENT_INFO_CLASS](../evntprov/ne-evntprov-event_info_class.md) of the
setting to be configured.

### -param pvInformation

The input buffer with the value of the setting to be configured. The format of
this buffer depends on the value of the _informationClass_ parameter.

### -param cbInformation

The size, in bytes, of the data in the input buffer.

## -returns

If you call this function from user-mode code, the function returns an
`HRESULT`. Use the `SUCCEEDED()` macro to determine whether the function
succeeds.

If you call this function from kernel-mode code, the function returns an
`NTSTATUS`. Use the `NT_SUCCESS()` macro to determine whether the function
succeeds.

## -remarks

This function serves as a wrapper around the
[EventSetInformation](../evntprov/nf-evntprov-eventsetinformation.md) function.

The **EventSetInformation** function is not available on all versions of
Windows. The default behavior of **TraceLoggingSetInformation** varies depending
on the target version of Windows (as controlled by compile-time WINVER and
NTDDI_VERSION macros): if the target version of Windows supports
**EventSetInformation** then **TraceLoggingSetInformation** will call the
function directly; otherwise, **TraceLoggingSetInformation** will attempt to
invoke **EventSetInformation** via GetProcAddress. To override the default
behavior of this function, set the `TLG_EVENT_SET_INFORMATION` and
`TLG_HAVE_EVENT_SET_INFORMATION` macros. Refer to the comments in the
TraceLoggingProvider.h header for details.

## -see-also

[TraceLoggingRegister](./nf-traceloggingprovider-traceloggingregister.md)

[EventSetInformation](../evntprov/nf-evntprov-eventsetinformation.md)

[EVENT_INFO_CLASS](../evntprov/ne-evntprov-event_info_class.md)

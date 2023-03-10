---
UID: NF:traceloggingprovider.TraceLoggingSetInformation
title: TraceLoggingSetInformation
description: Configures a TraceLogging provider by calling EventSetInformation.
ms.date: 06/06/2022
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
req.lib: Advapi32.lib
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
Windows. The default behavior of **TraceLoggingSetInformation** depends on the
compile-time values of the `WINVER` (user-mode) or `NTDDI_VERSION` (kernel-mode)
macros:

- If the target version of Windows (as specified by `WINVER` or `NTDDI_VERSION`)
  is known to support **EventSetInformation** then
  **TraceLoggingSetInformation** will directly invoke **EventSetInformation**.
- Otherwise, **TraceLoggingSetInformation** will use **GetProcAddress**
  (user-mode) or **MmGetSystemRoutineAddress** (kernel-mode) to locate and
  invoke **EventSetInformation**. If this fails, **TraceLoggingSetInformation**
  will return `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` (user-mode) or
  `STATUS_NOT_SUPPORTED` (kernel-mode).

To override the default behavior of this function, define the
`TLG_HAVE_EVENT_SET_INFORMATION` macro before you
`#include <TraceLoggingProvider.h>`:

- If you `#define TLG_HAVE_EVENT_SET_INFORMATION 0` then
  **TraceLoggingSetInformation** will do nothing and return
  `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` (user-mode) or
  `STATUS_ENTRYPOINT_NOT_FOUND` (kernel-mode).
- If you `#define TLG_HAVE_EVENT_SET_INFORMATION 1` then
  **TraceLoggingSetInformation** will directly invoke **EventSetInformation**.
- If you `#define TLG_HAVE_EVENT_SET_INFORMATION 2` then
  **TraceLoggingSetInformation** will invoke **EventSetInformation** via
  **GetProcAddress** (user-mode) or **MmGetSystemRoutineAddress** (kernel-mode).

For additional information, refer to the comments in the
`TraceLoggingProvider.h` header regarding the `TLG_HAVE_EVENT_SET_INFORMATION`
macro.

## -see-also

[TraceLoggingRegister](./nf-traceloggingprovider-traceloggingregister.md)

[EventSetInformation](../evntprov/nf-evntprov-eventsetinformation.md)

[EVENT_INFO_CLASS](../evntprov/ne-evntprov-event_info_class.md)

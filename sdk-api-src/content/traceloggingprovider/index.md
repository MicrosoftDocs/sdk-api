---
UID: NA:traceloggingprovider
title: TraceLoggingProvider.h header
ms.assetid: 9f0e53a0-c646-3851-b09a-e5e45c361a3c
ms.date: 06/06/2022
ms.keywords:
ms.topic: overview
ms.update-cycle: 1095-days
tech.root: tracelogging
f1_keywords:
  - traceloggingprovider
  - traceloggingprovider/traceloggingprovider
---

# TraceLoggingProvider.h header

## -description

[TraceLogging](../_tracelogging/index.md) is a system for logging
self-describing events that can be decoded without a manifest. On Windows,
TraceLogging is used to generate
[Event Tracing for Windows (ETW)](https://docs.microsoft.com/windows/win32/etw/about-event-tracing)
events.

The **TraceLoggingProvider.h** header in the Windows SDK has macros and inline
functions to generate TraceLogging-encoded ETW events for kernel and user-mode
code using C or C++.

> [!NOTE]
> **TraceLoggingProvider.h** requires compile-time constant values for
> event attributes such as provider name, event name, and field names. To
> minimize runtime overhead, **TraceLoggingProvider.h** builds its data
> structures at compile-time and stores the information in read-only memory. If
> you need to generate runtime-dynamic events, you will need to use a different
> TraceLogging implementation such as
> [TraceLoggingDynamic](https://github.com/microsoft/tracelogging/tree/main/etw).

## Quick Start

- In a .c or .cpp file, use the
  [**TRACELOGGING_DEFINE_PROVIDER**](./nf-traceloggingprovider-tracelogging_declare_provider.md)
  macro to declare a global provider handle. The provider handle represents your
  component's connection to ETW.
- At component startup (e.g. in `main`, `wmain`, `DllMain`, or `DriverEntry`),
  use the
  [**TraceLoggingRegister**](./nf-traceloggingprovider-traceloggingregister.md)
  function to open your component's connection to ETW.
- At component shutdown, use the
  [**TraceLoggingUnregister**](./nf-traceloggingprovider-traceloggingunregister.md)
  function to close your component's connection to ETW.
- During component execution, use the
  [**TraceLoggingWrite**](./nf-traceloggingprovider-traceloggingwrite.md) macro
  to generate TraceLogging-encoded ETW events.
- As needed, use the
  [**TRACELOGGING_DECLARE_PROVIDER**](./nf-traceloggingprovider-tracelogging_declare_provider.md)
  macro in headers to forward-declare the provider handle so it can be used in
  other parts of your component.
- Use tools like [WPR](/windows-hardware/test/wpt/introduction-to-wpr),
  [tracelog](/windows-hardware/drivers/devtest/tracelog), or
  [traceview](/windows-hardware/drivers/devtest/traceview) to collect traces.
- Use tools like [WPA](/windows-hardware/test/wpt/windows-performance-analyzer),
  [tracefmt](/windows-hardware/drivers/devtest/tracefmt), or
  [traceview](/windows-hardware/drivers/devtest/traceview) to decode and view
  traces.

### Example

```c
#include <windows.h> // or <wdm.h> for kernel-mode.
#include <winmeta.h> // For event level definitions.
#include <TraceLoggingProvider.h>

TRACELOGGING_DEFINE_PROVIDER( // defines g_hProvider
    g_hProvider, // Name of the provider handle
    "MyCompany.MyComponent", // Human-readable name for the provider
    // {ce5fa4ea-ab00-5402-8b76-9f76ac858fb5}
    (0xce5fa4ea,0xab00,0x5402,0x8b,0x76,0x9f,0x76,0xac,0x85,0x8f,0xb5));

int main(int argc, char* argv[]) // or DriverEntry for kernel-mode.
{
    TraceLoggingRegister(g_hProvider);

    TraceLoggingWrite(
        g_hProvider,
        "MyEvent1",
        TraceLoggingLevel(WINEVENT_LEVEL_WARNING), // Levels defined in <winmeta.h>
        TraceLoggingKeyword(MyEventCategories), // Provider-defined categories
        TraceLoggingString(argv[0], "arg0"), // field name is "arg0"
        TraceLoggingInt32(argc)); // field name is implicitly "argc"

    TraceLoggingUnregister(g_hProvider);
    return 0;
}
```

For more information, see:

- [TraceLogging](../_tracelogging/index.md)
- [TraceLogging wrapper macros](/windows/desktop/tracelogging/tracelogging-wrapper-macros)
- [TraceLoggingWrite](./nf-traceloggingprovider-traceloggingwrite.md)
- [TRACELOGGING_DECLARE_PROVIDER](./nf-traceloggingprovider-tracelogging_declare_provider.md)
- [TRACELOGGING_DEFINE_PROVIDER](./nf-traceloggingprovider-tracelogging_define_provider.md)

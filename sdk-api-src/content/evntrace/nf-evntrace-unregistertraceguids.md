---
UID: NF:evntrace.UnregisterTraceGuids
title: UnregisterTraceGuids function (evntrace.h)
description:
  Unregisters a "Classic" (Windows 2000-style) ETW event trace provider that was
  registered using RegisterTraceGuids.
helpviewer_keywords:
  [
    "UnregisterTraceGuids",
    "UnregisterTraceGuids function [ETW]",
    "_evt_unregistertraceguids",
    "base.unregistertraceguids",
    "etw.unregistertraceguids",
    "evntrace/UnregisterTraceGuids",
  ]
old-location: etw\unregistertraceguids.htm
tech.root: ETW
ms.assetid: 1fa10f66-a78b-4f40-9518-72d48365246e
ms.date: 12/05/2018
ms.keywords:
  UnregisterTraceGuids, UnregisterTraceGuids function [ETW],
  _evt_unregistertraceguids, base.unregistertraceguids,
  etw.unregistertraceguids, evntrace/UnregisterTraceGuids
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - UnregisterTraceGuids
  - evntrace/UnregisterTraceGuids
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - Advapi32.dll
  - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
  - KernelBase.dll
  - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
  - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
  - UnregisterTraceGuids
---

# UnregisterTraceGuids function

## -description

The **UnregisterTraceGuids** function unregisters a
[Classic](/windows/win32/etw/tracing-events) (Windows 2000-style) ETW event
trace provider that was registered using
[RegisterTraceGuids](/windows/desktop/ETW/registertraceguids).

## -parameters

### -param RegistrationHandle [in]

Handle to the event trace provider, obtained from an earlier call to the
[RegisterTraceGuids](/windows/desktop/ETW/registertraceguids) function.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_INVALID_PARAMETER**

  The _RegistrationHandle_ parameter does not specify the handle to a registered
  provider or is **NULL**.

## -remarks

Providers call this function.

The event trace provider must have been registered previously by calling the
[RegisterTraceGuids](/windows/desktop/ETW/registertraceguids) function.

> [!Important]
> All registration handles created by a DLL or driver must be
> unregistered before the DLL or driver unloads. If the provider is not
> unregistered, a crash will occur when ETW tries to invoke the provider's
> callback.

## -see-also

[RegisterTraceGuids](/windows/desktop/ETW/registertraceguids)

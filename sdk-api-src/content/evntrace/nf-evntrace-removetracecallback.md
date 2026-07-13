---
UID: NF:evntrace.RemoveTraceCallback
title: RemoveTraceCallback function (evntrace.h)
description:
  The RemoveTraceCallback function stops an EventCallback function from
  receiving events for an event trace class. This function is obsolete.
helpviewer_keywords:
  [
    "RemoveTraceCallback",
    "RemoveTraceCallback function [ETW]",
    "_evt_removetracecallback",
    "base.removetracecallback",
    "etw.removetracecallback",
    "evntrace/RemoveTraceCallback",
  ]
old-location: etw\removetracecallback.htm
tech.root: ETW
ms.assetid: da779e8d-4984-44e3-8731-647a422b55b2
ms.date: 12/05/2018
ms.keywords:
  RemoveTraceCallback, RemoveTraceCallback function [ETW],
  _evt_removetracecallback, base.removetracecallback, etw.removetracecallback,
  evntrace/RemoveTraceCallback
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: AdvAPI32.Lib
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - RemoveTraceCallback
  - evntrace/RemoveTraceCallback
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Obsolete-l1-1-0.dll
 - KernelBase.dll
api_name:
  - RemoveTraceCallback
---

# RemoveTraceCallback function

## -description

> [!Important]
> Do not use this function. It may be unavailable in subsequent
> versions.

The **RemoveTraceCallback** function stops an
[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)
function from receiving events for an event trace class.

## -parameters

### -param pGuid [in]

Pointer to the class GUID of the event trace class for which the callback
receives events. Use the same class GUID that you passed to the
[SetTraceCallback](/windows/desktop/ETW/settracecallback) to begin receiving the
events.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_INVALID_PARAMETER**

  The _pGuid_ parameter is **NULL**.

- **ERROR_WMI_GUID_NOT_FOUND**

  There is no
  [EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)
  function associated with the event trace class.

## -remarks

Consumers call this function.

## -see-also

[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)

[ProcessTrace](/windows/desktop/ETW/processtrace)

[SetTraceCallback](/windows/desktop/ETW/settracecallback)

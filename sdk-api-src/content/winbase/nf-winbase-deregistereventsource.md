---
UID: NF:winbase.DeregisterEventSource
title: DeregisterEventSource function (winbase.h)
description: Closes the specified event log. (DeregisterEventSource)
helpviewer_keywords: ["DeregisterEventSource","DeregisterEventSource function","_win32_deregistereventsource","base.deregistereventsource","winbase/DeregisterEventSource"]
old-location: base\deregistereventsource.htm
tech.root: base
ms.assetid: f5d1f4b0-5320-4aec-a129-cafff6f1fed1
ms.date: 12/05/2018
ms.keywords: DeregisterEventSource, DeregisterEventSource function, _win32_deregistereventsource, base.deregistereventsource, winbase/DeregisterEventSource
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeregisterEventSource
 - winbase/DeregisterEventSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-advapi32-eventlog-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-EventLog-Legacy-l1-1-0.dll
 - advapi32legacy.dll
 - Ext-MS-Win-AdvAPI32-EventLog-l1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - DeregisterEventSource
---

# DeregisterEventSource function


## -description

Closes the specified event log.

## -parameters

### -param hEventLog [in, out]

A handle to the event log. The 
<a href="/windows/desktop/api/winbase/nf-winbase-registereventsourcea">RegisterEventSource</a> function returns this handle.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/EventLog/event-sources">Event Sources</a>



<a href="/windows/desktop/api/winbase/nf-winbase-registereventsourcea">RegisterEventSource</a>

---
UID: NF:winbase.NotifyChangeEventLog
title: NotifyChangeEventLog function (winbase.h)
description: Enables an application to receive notification when an event is written to the specified event log.
helpviewer_keywords: ["NotifyChangeEventLog","NotifyChangeEventLog function","_win32_notifychangeeventlog","base.notifychangeeventlog","winbase/NotifyChangeEventLog"]
old-location: base\notifychangeeventlog.htm
tech.root: base
ms.assetid: 12b9a7bf-2aad-48b7-8cfd-a72b353ba2b2
ms.date: 12/05/2018
ms.keywords: NotifyChangeEventLog, NotifyChangeEventLog function, _win32_notifychangeeventlog, base.notifychangeeventlog, winbase/NotifyChangeEventLog
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
 - NotifyChangeEventLog
 - winbase/NotifyChangeEventLog
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
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - NotifyChangeEventLog
req.apiset: ext-ms-win-advapi32-eventlog-l1-1-1 (introduced in Windows 10, version 10.0.10240)
---

# NotifyChangeEventLog function


## -description

Enables an application to receive notification when an event is written to the specified event log. When the event is written to the log, the specified event object is set to the signaled state.

## -parameters

### -param hEventLog [in]

A handle to an event log. The 
<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>  function returns this handle.

### -param hEvent [in]

A handle to a manual-reset or auto-reset event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create the event object.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>NotifyChangeEventLog</b> function does not work with remote handles. If the <i>hEventLog</i> parameter is the handle to an event log on a remote computer, <b>NotifyChangeEventLog</b> returns zero, and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>.

If the thread is not waiting on the event when the system calls <a href="/windows/desktop/api/winbase/nf-winbase-pulseevent">PulseEvent</a>, the thread will not receive the notification. Therefore, you should create a separate thread to wait for notifications.

The system will continue to notify you of changes until you close the handle to the event log. To close the event log, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-closeeventlog">CloseEventLog</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-deregistereventsource">DeregisterEventSource</a> function.


#### Examples

For an example, see <a href="/windows/desktop/EventLog/receiving-event-notification">Receiving Event Notification</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-closeeventlog">CloseEventLog</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deregistereventsource">DeregisterEventSource</a>



<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>

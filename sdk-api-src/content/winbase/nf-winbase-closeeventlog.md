---
UID: NF:winbase.CloseEventLog
title: CloseEventLog function (winbase.h)
description: Closes the specified event log. (CloseEventLog)
helpviewer_keywords: ["CloseEventLog","CloseEventLog function","_win32_closeeventlog","base.closeeventlog","winbase/CloseEventLog"]
old-location: base\closeeventlog.htm
tech.root: base
ms.assetid: cb98a0cf-8ee9-4d78-8508-efae1d43a91d
ms.date: 12/05/2018
ms.keywords: CloseEventLog, CloseEventLog function, _win32_closeeventlog, base.closeeventlog, winbase/CloseEventLog
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
 - CloseEventLog
 - winbase/CloseEventLog
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
 - Ext-MS-Win-AdvAPI32-EventLog-l1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - CloseEventLog
req.apiset: ext-ms-win-advapi32-eventlog-l1-1-0 (introduced in Windows 8)
---

# CloseEventLog function


## -description

Closes the specified event log.

## -parameters

### -param hEventLog [in, out]

A handle to the event log to be closed. The 
<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-openbackupeventloga">OpenBackupEventLog</a> function returns this handle.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>

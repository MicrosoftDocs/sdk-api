---
UID: NF:winbase.GetOldestEventLogRecord
title: GetOldestEventLogRecord function (winbase.h)
description: Retrieves the absolute record number of the oldest record in the specified event log.
helpviewer_keywords: ["GetOldestEventLogRecord","GetOldestEventLogRecord function","_win32_getoldesteventlogrecord","base.getoldesteventlogrecord","winbase/GetOldestEventLogRecord"]
old-location: base\getoldesteventlogrecord.htm
tech.root: base
ms.assetid: 2f64f82b-a5f5-4701-844b-5979a0124414
ms.date: 12/05/2018
ms.keywords: GetOldestEventLogRecord, GetOldestEventLogRecord function, _win32_getoldesteventlogrecord, base.getoldesteventlogrecord, winbase/GetOldestEventLogRecord
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
 - GetOldestEventLogRecord
 - winbase/GetOldestEventLogRecord
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
 - GetOldestEventLogRecord
req.apiset: ext-ms-win-advapi32-eventlog-l1-1-1 (introduced in Windows 10, version 10.0.10240)
---

# GetOldestEventLogRecord function


## -description

Retrieves the absolute record number of the oldest record in the specified event log.

## -parameters

### -param hEventLog [in]

A handle to the open event log. The 
<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-openbackupeventloga">OpenBackupEventLog</a> function returns this handle.

### -param OldestRecord [out]

A pointer to a variable that receives the absolute record number of the oldest record in the specified event log.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The oldest record in an event log is not necessarily record number 1. For more information, see 
<a href="/windows/desktop/EventLog/event-log-records">Event Log Records</a>.


#### Examples

For an example, see 
<a href="/windows/desktop/EventLog/querying-for-event-source-messages">Querying for Event Information</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getnumberofeventlogrecords">GetNumberOfEventLogRecords</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openbackupeventloga">OpenBackupEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>

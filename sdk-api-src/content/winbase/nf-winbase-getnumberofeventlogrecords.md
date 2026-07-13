---
UID: NF:winbase.GetNumberOfEventLogRecords
title: GetNumberOfEventLogRecords function (winbase.h)
description: Retrieves the number of records in the specified event log.
helpviewer_keywords: ["GetNumberOfEventLogRecords","GetNumberOfEventLogRecords function","_win32_getnumberofeventlogrecords","base.getnumberofeventlogrecords","winbase/GetNumberOfEventLogRecords"]
old-location: base\getnumberofeventlogrecords.htm
tech.root: base
ms.assetid: 80cc8735-26a2-4ad3-a111-28f2c0c52e98
ms.date: 12/05/2018
ms.keywords: GetNumberOfEventLogRecords, GetNumberOfEventLogRecords function, _win32_getnumberofeventlogrecords, base.getnumberofeventlogrecords, winbase/GetNumberOfEventLogRecords
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
 - GetNumberOfEventLogRecords
 - winbase/GetNumberOfEventLogRecords
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
 - GetNumberOfEventLogRecords
req.apiset: ext-ms-win-advapi32-eventlog-l1-1-1 (introduced in Windows 10, version 10.0.10240)
---

# GetNumberOfEventLogRecords function


## -description

Retrieves the number of records in the specified event log.

## -parameters

### -param hEventLog [in]

A handle to the open event log. The 
<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-openbackupeventloga">OpenBackupEventLog</a> function returns this handle.

### -param NumberOfRecords [out]

A pointer to a variable that receives the number of records in the specified event log.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The oldest record in an event log is not necessarily record number 1. To determine the oldest record number in an event log, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getoldesteventlogrecord">GetOldestEventLogRecord</a> function.

## -see-also

<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getoldesteventlogrecord">GetOldestEventLogRecord</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openbackupeventloga">OpenBackupEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>

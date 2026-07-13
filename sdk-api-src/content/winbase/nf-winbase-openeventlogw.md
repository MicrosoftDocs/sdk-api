---
UID: NF:winbase.OpenEventLogW
title: OpenEventLogW function (winbase.h)
description: Opens a handle to the specified event log. (Unicode)
helpviewer_keywords: ["OpenEventLog", "OpenEventLog function", "OpenEventLogW", "_win32_openeventlog", "base.openeventlog", "winbase/OpenEventLog", "winbase/OpenEventLogW"]
old-location: base\openeventlog.htm
tech.root: base
ms.assetid: 6cd8797a-aeaf-4603-b43c-b1ff45b6200a
ms.date: 12/05/2018
ms.keywords: OpenEventLog, OpenEventLog function, OpenEventLogA, OpenEventLogW, _win32_openeventlog, base.openeventlog, winbase/OpenEventLog, winbase/OpenEventLogA, winbase/OpenEventLogW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenEventLogW (Unicode) and OpenEventLogA (ANSI)
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
 - OpenEventLogW
 - winbase/OpenEventLogW
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
 - Ext-Ms-Win-AdvAPI32-EventLog-Ansi-L1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - OpenEventLog
 - OpenEventLogA
 - OpenEventLogW
req.apiset: ext-ms-win-advapi32-eventlog-ansi-l1-1-0 (introduced in Windows 10, version 10.0.10240)
---

# OpenEventLogW function


## -description

Opens a handle to the specified event log.

## -parameters

### -param lpUNCServerName [in]

The Universal Naming Convention (UNC) name of the remote server on which the event log is to be opened. If this parameter is <b>NULL</b>, the local computer is used.

### -param lpSourceName [in]

The name of the log. 

If you specify a custom log and it cannot be found, the event logging service opens the <b>Application</b> log; however, there will be no associated message or category string file.

## -returns

If the function succeeds, the return value is the handle to an event log.
						

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To close the handle to the event log, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-closeeventlog">CloseEventLog</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/EventLog/querying-for-event-source-messages">Querying for Event Information</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines OpenEventLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-cleareventloga">ClearEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-closeeventlog">CloseEventLog</a>



<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/EventLog/eventlog-key">Eventlog Key</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readeventloga">ReadEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-reporteventa">ReportEvent</a>

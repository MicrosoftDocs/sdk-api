---
UID: NF:winbase.ReadEventLogW
title: ReadEventLogW function (winbase.h)
description: Reads the specified number of entries from the specified event log. (Unicode)
helpviewer_keywords: ["EVENTLOG_BACKWARDS_READ", "EVENTLOG_FORWARDS_READ", "EVENTLOG_SEEK_READ", "EVENTLOG_SEQUENTIAL_READ", "ReadEventLog", "ReadEventLog function", "ReadEventLogW", "_win32_readeventlog", "base.readeventlog", "winbase/ReadEventLog", "winbase/ReadEventLogW"]
old-location: base\readeventlog.htm
tech.root: base
ms.assetid: 10b37174-661a-4dc6-a7fe-752739494156
ms.date: 12/05/2018
ms.keywords: EVENTLOG_BACKWARDS_READ, EVENTLOG_FORWARDS_READ, EVENTLOG_SEEK_READ, EVENTLOG_SEQUENTIAL_READ, ReadEventLog, ReadEventLog function, ReadEventLogA, ReadEventLogW, _win32_readeventlog, base.readeventlog, winbase/ReadEventLog, winbase/ReadEventLogA, winbase/ReadEventLogW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReadEventLogW (Unicode) and ReadEventLogA (ANSI)
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
 - ReadEventLogW
 - winbase/ReadEventLogW
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
 - Ext-MS-Win-AdvAPI32-EventLog-L1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-Ansi-L1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - ReadEventLog
 - ReadEventLogA
 - ReadEventLogW
req.apiset: ext-ms-win-advapi32-eventlog-ansi-l1-1-0 (introduced in Windows 10, version 10.0.10240)
---

# ReadEventLogW function


## -description

Reads the specified number of entries from the specified event log. The function can be used to read log entries in chronological or reverse chronological order.

## -parameters

### -param hEventLog [in]

A handle to the event log to be read. The 
<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> function returns this handle.

### -param dwReadFlags [in]

Use the following flag values to indicate how to read the log file. This parameter must include one of the following values (the flags are mutually exclusive). 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_SEEK_READ"></a><a id="eventlog_seek_read"></a><dl>
<dt><b>EVENTLOG_SEEK_READ</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Begin reading from the record specified in the <i>dwRecordOffset</i> parameter. 




This option may  not work with large log files if the function cannot determine the log file's size. For details, see Knowledge Base article, 177199.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_SEQUENTIAL_READ"></a><a id="eventlog_sequential_read"></a><dl>
<dt><b>EVENTLOG_SEQUENTIAL_READ</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Read the records sequentially. 



If this is the first read operation, the EVENTLOG_FORWARDS_READ EVENTLOG_BACKWARDS_READ flags determines which record is read first.

</td>
</tr>
</table>
 

You must specify one of the following flags to indicate the direction for successive read operations (the flags are mutually exclusive).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_FORWARDS_READ"></a><a id="eventlog_forwards_read"></a><dl>
<dt><b>EVENTLOG_FORWARDS_READ</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The log is read in chronological order (oldest to newest). 

The default.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_BACKWARDS_READ"></a><a id="eventlog_backwards_read"></a><dl>
<dt><b>EVENTLOG_BACKWARDS_READ</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The log is read in reverse chronological order (newest to oldest). 



							

</td>
</tr>
</table>

### -param dwRecordOffset [in]

The record number of the log-entry at which the read operation should start. This parameter is ignored unless <i>dwReadFlags</i> includes the <b>EVENTLOG_SEEK_READ</b> flag.

### -param lpBuffer [out]

An application-allocated buffer that will receive one or more <a href="/windows/desktop/api/winnt/ns-winnt-eventlogrecord">EVENTLOGRECORD</a> structures. This parameter cannot be <b>NULL</b>, even if the <i>nNumberOfBytesToRead</i> parameter is zero. 




The maximum size of this buffer is 0x7ffff bytes.

### -param nNumberOfBytesToRead [in]

The size of the <i>lpBuffer</i> buffer, in bytes. This function will read as many log entries as will fit in the buffer; the function will not return partial entries.

### -param pnBytesRead [out]

A pointer to a variable that receives the number of bytes read by the function.

### -param pnMinNumberOfBytesNeeded [out]

A pointer to a variable that receives the required size of the <i>lpBuffer</i> buffer. This value is valid only this function returns zero and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When this function returns successfully, the read position in the event  log is adjusted by the number of records read.

<div class="alert"><b>Note</b>  The configured file name for this source may also be the configured file name for other sources (several sources can exist as subkeys under a single log). Therefore, this function may return events that were logged by more than one source.</div>
<div> </div>

#### Examples

For an example, see 
<a href="/windows/desktop/EventLog/querying-for-event-source-messages">Querying for Event Information</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines ReadEventLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-cleareventloga">ClearEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-closeeventlog">CloseEventLog</a>



<a href="/windows/desktop/api/winnt/ns-winnt-eventlogrecord">EVENTLOGRECORD</a>



<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-reporteventa">ReportEvent</a>

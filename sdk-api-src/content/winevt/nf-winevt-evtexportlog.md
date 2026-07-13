---
UID: NF:winevt.EvtExportLog
title: EvtExportLog function (winevt.h)
description: Copies events from the specified channel or log file and writes them to the target log file.
helpviewer_keywords: ["EvtExportLog","EvtExportLog function [EventLog]","wes.evtexportlog","winevt/EvtExportLog"]
old-location: wes\evtexportlog.htm
tech.root: wes
ms.assetid: c177029f-84e3-41ec-bbdb-26b0c1bf481f
ms.date: 12/05/2018
ms.keywords: EvtExportLog, EvtExportLog function [EventLog], wes.evtexportlog, winevt/EvtExportLog
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtExportLog
 - winevt/EvtExportLog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtExportLog
---

# EvtExportLog function


## -description

Copies events from the specified channel or log file and writes them to the target log file.

## -parameters

### -param Session [in, optional]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> for local channels.

### -param Path [in]

The name of the channel or the full path to a log file that contains the events that you want to export. If the <i>Query</i> parameter contains an XPath query, you must specify the channel or log file. If the <i>Flags</i> parameter contains EvtExportLogFilePath, you must specify the log file. If the <i>Query</i> parameter contains a structured XML query, the channel or path that you specify here must match the channel or path in the query. If the <i>Flags</i> parameter contains EvtExportLogChannelPath, this parameter can be <b>NULL</b> if  the query is a structured XML query that specifies the channel.

### -param Query [in]

A query that specifies the types of events that you want to export. You can specify an XPath 1.0 query or structured XML query. If your XPath contains more than 20 expressions, use a structured XML query. To export all events, set this parameter to <b>NULL</b> or "*".

### -param TargetFilePath [in]

The full path to the target log file that will receive the events. The target log file must not exist.

### -param Flags [in]

Flags that indicate whether the events come from a channel or log file. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_exportlog_flags">EVT_EXPORTLOG_FLAGS</a> enumeration.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. Use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

</td>
</tr>
</table>

## -remarks

You can export events from multiple channels using a structured XML query (see <a href="/windows/desktop/WES/consuming-events">Consuming Events</a>); however, you cannot use this function to merge events from multiple log files. If the query result is empty, the service creates a file that contains header information but no events.

To remove events from a channel and write them to a target log file, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclearlog">EvtClearLog</a> function. To include localized strings with the events in the log file, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtarchiveexportedlog">EvtArchiveExportedLog</a> function.

You must specify the absolute path to the target log file; you cannot use relative paths and environment variables to specifying the target log file.  The path can be a Universal Naming Convention (UNC) path. You should use .evtx as the file name extension.

This function  affects only the specified channel or log file—if the channel uses autoBackup or fileMax, this function will not affect those backup files.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/saving-events-to-a-log-file">Saving Events to a Log File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtarchiveexportedlog">EvtArchiveExportedLog</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtclearlog">EvtClearLog</a>
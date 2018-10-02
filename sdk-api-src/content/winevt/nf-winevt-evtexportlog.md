---
UID: NF:winevt.EvtExportLog
title: EvtExportLog function
author: windows-sdk-content
description: Copies events from the specified channel or log file and writes them to the target log file.
old-location: wes\evtexportlog.htm
tech.root: WES
ms.assetid: c177029f-84e3-41ec-bbdb-26b0c1bf481f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EvtExportLog, EvtExportLog function [EventLog], wes.evtexportlog, winevt/EvtExportLog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtExportLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtExportLog function


## -description


Copies events from the specified channel or log file and writes them to the target log file.


## -parameters




### -param Session [in, optional]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> for local channels.


### -param Path [in]

The name of the channel or the full path to a log file that contains the events that you want to export. If the <i>Query</i> parameter contains an XPath query, you must specify the channel or log file. If the <i>Flags</i> parameter contains EvtExportLogFilePath, you must specify the log file. If the <i>Query</i> parameter contains a structured XML query, the channel or path that you specify here must match the channel or path in the query. If the <i>Flags</i> parameter contains EvtExportLogChannelPath, this parameter can be <b>NULL</b> if  the query is a structured XML query that specifies the channel.


### -param Query [in]

A query that specifies the types of events that you want to export. You can specify an XPath 1.0 query or structured XML query. If your XPath contains more than 20 expressions, use a structured XML query. To export all events, set this parameter to <b>NULL</b> or "*".


### -param TargetFilePath [in]

The full path to the target log file that will receive the events. The target log file must not exist.


### -param Flags [in]

Flags that indicate whether the events come from a channel or log file. For possible values, see the <a href="https://msdn.microsoft.com/02a63a3c-5c9b-485f-bd52-a97c40cb83d1">EVT_EXPORTLOG_FLAGS</a> enumeration.


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
The function failed. Use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.

</td>
</tr>
</table>
 




## -remarks



You can export events from multiple channels using a structured XML query (see <a href="https://msdn.microsoft.com/17204d3f-0875-42c5-9af4-caca6349a67d">Consuming Events</a>); however, you cannot use this function to merge events from multiple log files. If the query result is empty, the service creates a file that contains header information but no events.

To remove events from a channel and write them to a target log file, call the <a href="https://msdn.microsoft.com/26d2aabd-96dc-4091-82f4-e5d4c69e09a4">EvtClearLog</a> function. To include localized strings with the events in the log file, call the <a href="https://msdn.microsoft.com/0a8f9958-03af-4310-9f9e-b79e84a30a04">EvtArchiveExportedLog</a> function.

You must specify the absolute path to the target log file; you cannot use relative paths and environment variables to specifying the target log file.  The path can be a Universal Naming Convention (UNC) path. You should use .evtx as the file name extension.

This function  affects only the specified channel or log file—if the channel uses autoBackup or fileMax, this function will not affect those backup files.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/6d71ed15-97e3-4888-b161-c7e31bf3fc6d">Saving Events to a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0a8f9958-03af-4310-9f9e-b79e84a30a04">EvtArchiveExportedLog</a>



<a href="https://msdn.microsoft.com/26d2aabd-96dc-4091-82f4-e5d4c69e09a4">EvtClearLog</a>
 

 


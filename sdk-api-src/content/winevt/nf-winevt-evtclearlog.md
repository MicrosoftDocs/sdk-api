---
UID: NF:winevt.EvtClearLog
title: EvtClearLog function (winevt.h)
description: Removes all events from the specified channel and writes them to the target log file.
helpviewer_keywords: ["EvtClearLog","EvtClearLog function [EventLog]","wes.evtclearlog","winevt/EvtClearLog"]
old-location: wes\evtclearlog.htm
tech.root: wes
ms.assetid: 26d2aabd-96dc-4091-82f4-e5d4c69e09a4
ms.date: 12/05/2018
ms.keywords: EvtClearLog, EvtClearLog function [EventLog], wes.evtclearlog, winevt/EvtClearLog
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
 - EvtClearLog
 - winevt/EvtClearLog
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
api_name:
 - EvtClearLog
---

# EvtClearLog function


## -description

Removes all events from the specified channel and writes them to the target log file.

## -parameters

### -param Session [in, optional]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> for local channels.

### -param ChannelPath [in]

The name of the channel to clear.

### -param TargetFilePath [in, optional]

The full path to the target log file that will receive the events. Set to <b>NULL</b> to clear the log file and not save the events.

### -param Flags [in]

Reserved. Must be zero.

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

To copy events from a channel or log file, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtexportlog">EvtExportLog</a> function.

You must specify the absolute path to the target log file; you cannot use relative paths and environment variables to specifying the target log file.  The path can be a Universal Naming Convention (UNC) path. You should use .evtx as the file name extension.

This function affects only the channel—if the channel uses autoBackup or fileMax, this function will not affect those backup files.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtarchiveexportedlog">EvtArchiveExportedLog</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtexportlog">EvtExportLog</a>
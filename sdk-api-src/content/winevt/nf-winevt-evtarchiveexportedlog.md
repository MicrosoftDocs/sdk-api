---
UID: NF:winevt.EvtArchiveExportedLog
title: EvtArchiveExportedLog function (winevt.h)
description: Adds localized strings to the events in the specified log file.
helpviewer_keywords: ["EvtArchiveExportedLog","EvtArchiveExportedLog function [EventLog]","wes.evtarchiveexportedlog","winevt/EvtArchiveExportedLog"]
old-location: wes\evtarchiveexportedlog.htm
tech.root: wes
ms.assetid: 0a8f9958-03af-4310-9f9e-b79e84a30a04
ms.date: 12/05/2018
ms.keywords: EvtArchiveExportedLog, EvtArchiveExportedLog function [EventLog], wes.evtarchiveexportedlog, winevt/EvtArchiveExportedLog
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
 - EvtArchiveExportedLog
 - winevt/EvtArchiveExportedLog
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
 - EvtArchiveExportedLog
---

# EvtArchiveExportedLog function


## -description

Adds localized strings to the events in the specified log file.

## -parameters

### -param Session [in]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> for local channels.

### -param LogFilePath [in]

The full path to the exported log file that contains the events to localize.

### -param Locale [in]

The locale to use to localize the strings that the service adds to the events in the log file. If zero, the function uses the calling thread's locale. If the provider's resources does not contain the locale, the string is empty.

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

To consume an event from an exported log file, the provider needs to be available to provide the resources (message strings) for the event. You would call this function to include the localized resources with the event, so that you can consume the event when the provider is not available.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtclearlog">EvtClearLog</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtexportlog">EvtExportLog</a>
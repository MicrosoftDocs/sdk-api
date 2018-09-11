---
UID: NF:winevt.EvtArchiveExportedLog
title: EvtArchiveExportedLog function
author: windows-sdk-content
description: Adds localized strings to the events in the specified log file.
old-location: wes\evtarchiveexportedlog.htm
tech.root: WES
ms.assetid: 0a8f9958-03af-4310-9f9e-b79e84a30a04
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EvtArchiveExportedLog, EvtArchiveExportedLog function [EventLog], wes.evtarchiveexportedlog, winevt/EvtArchiveExportedLog
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
api_name:
 - EvtArchiveExportedLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtArchiveExportedLog function


## -description


Adds localized strings to the events in the specified log file.


## -parameters




### -param Session [in]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> for local channels.


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
The function failed. Use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.

</td>
</tr>
</table>
 




## -remarks



To consume an event from an exported log file, the provider needs to be available to provide the resources (message strings) for the event. You would call this function to include the localized resources with the event, so that you can consume the event when the provider is not available.




## -see-also




<a href="https://msdn.microsoft.com/26d2aabd-96dc-4091-82f4-e5d4c69e09a4">EvtClearLog</a>



<a href="https://msdn.microsoft.com/c177029f-84e3-41ec-bbdb-26b0c1bf481f">EvtExportLog</a>
 

 


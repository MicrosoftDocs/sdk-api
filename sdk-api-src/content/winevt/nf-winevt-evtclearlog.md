---
UID: NF:winevt.EvtClearLog
title: EvtClearLog function
author: windows-driver-content
description: Removes all events from the specified channel and writes them to the target log file.
old-location: wes\evtclearlog.htm
old-project: WES
ms.assetid: 26d2aabd-96dc-4091-82f4-e5d4c69e09a4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EvtClearLog, EvtClearLog function [EventLog], wes.evtclearlog, winevt/EvtClearLog
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
req.typenames: EVT_VARIANT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wevtapi.dll
api_name:
-	EvtClearLog
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EvtClearLog function


## -description


Removes all events from the specified channel and writes them to the target log file.


## -parameters




### -param Session [in, optional]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> for local channels.


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
The function failed. Use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.

</td>
</tr>
</table>
 




## -remarks



To copy events from a channel or log file, call the <a href="https://msdn.microsoft.com/c177029f-84e3-41ec-bbdb-26b0c1bf481f">EvtExportLog</a> function.

You must specify the absolute path to the target log file; you cannot use relative paths and environment variables to specifying the target log file.  The path can be a Universal Naming Convention (UNC) path. You should use .evtx as the file name extension.

This function affects only the channel—if the channel uses autoBackup or fileMax, this function will not affect those backup files.




## -see-also




<a href="https://msdn.microsoft.com/0a8f9958-03af-4310-9f9e-b79e84a30a04">EvtArchiveExportedLog</a>



<a href="https://msdn.microsoft.com/c177029f-84e3-41ec-bbdb-26b0c1bf481f">EvtExportLog</a>
 

 


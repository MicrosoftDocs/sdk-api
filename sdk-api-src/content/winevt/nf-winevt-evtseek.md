---
UID: NF:winevt.EvtSeek
title: EvtSeek function
author: windows-sdk-content
description: Seeks to a specific event in a query result set.
old-location: wes\evtseek.htm
tech.root: wes
ms.assetid: 62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: EvtSeek, EvtSeek function [EventLog], wes.evtseek, winevt/EvtSeek
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
 - EvtSeek
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtSeek function


## -description


Seeks to a specific event in a query result set.


## -parameters




### -param ResultSet [in]

The handle to a query result set that the <a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a> function returns.


### -param Position [in]

The zero-based offset to an event in the result set. The flag that you specify in the <i>Flags</i> parameter indicates the beginning relative position in the result set from which to seek. For example, you can seek from the beginning of the results or from the end of the results. Set to 0 to move to the relative position specified by the flag.


### -param Bookmark [in]

A handle to a bookmark that the <a href="https://msdn.microsoft.com/1020d923-090b-48fc-96c2-394db5cd241e">EvtCreateBookmark</a> function returns. The bookmark identifies an event in the result set to which you want to seek. Set this parameter only if the  <i>Flags</i> parameter has the EvtSeekRelativeToBookmark  flag set.


### -param Timeout [in]

 Reserved. Must be zero. 


### -param Flags [in]

One or more flags that indicate the relative position in the result set from which to seek. For possible values, see the <a href="https://msdn.microsoft.com/5340815b-b94a-488b-bfa1-01dcbc15e505">EVT_SEEK_FLAGS</a> enumeration.


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
The function was successful.

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
The function failed. To get the error code, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

</td>
</tr>
</table>
 




## -remarks



You can use this function only on result sets from an Admin or Operational channel, or from .evtx log files.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/e7eeafc3-deb9-4cdc-9763-f784db7333be">Bookmarking Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/46d40734-f022-4775-aa4f-13f4069c43c8">EvtNext</a>



<a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a>
 

 


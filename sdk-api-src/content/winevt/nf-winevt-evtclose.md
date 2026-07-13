---
UID: NF:winevt.EvtClose
title: EvtClose function (winevt.h)
description: Closes an open handle.
helpviewer_keywords: ["EvtClose","EvtClose function [EventLog]","wes.evtclose","winevt/EvtClose"]
old-location: wes\evtclose.htm
tech.root: wes
ms.assetid: c4b82d7b-508d-45bf-b990-04e90e846525
ms.date: 12/05/2018
ms.keywords: EvtClose, EvtClose function [EventLog], wes.evtclose, winevt/EvtClose
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
 - EvtClose
 - winevt/EvtClose
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
 - EvtClose
---

# EvtClose function


## -description

Closes an open handle.

## -parameters

### -param Object [in]

An open event handle to close.

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
The function succeeded

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
The function failed. To get the error code, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

</td>
</tr>
</table>

## -remarks

 You cannot use the handle after the handle is closed. When you close a parent handle, any opened handles that were created using the handle are also closed. For example, if you query for events, the query result contains a handle for each event that matches the query. Best practice suggests that you close each event handle when you are done with the event but if you do not, when you close the query handle, all event handles are also closed.
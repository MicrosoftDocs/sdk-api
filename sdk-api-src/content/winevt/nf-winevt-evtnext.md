---
UID: NF:winevt.EvtNext
title: EvtNext function
author: windows-sdk-content
description: Gets the next event from the query or subscription results.
old-location: wes\evtnext.htm
tech.root: wes
ms.assetid: 46d40734-f022-4775-aa4f-13f4069c43c8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EvtNext, EvtNext function [EventLog], wes.evtnext, winevt/EvtNext
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
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtNext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtNext function


## -description


Gets the next event from the query or subscription results.


## -parameters




### -param ResultSet [in]

The handle to a query or subscription result set that the <a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a> function or the <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> function returns.


### -param EventsSize [in]

The number of elements in the <i>EventArray</i> array. The function will try to retrieve this number of elements from the result set.


### -param Events [in]

A pointer to an array of handles that will be set to the handles to the events from the result set.


### -param Timeout [in]

The number of milliseconds that you are willing to wait for a result.  Set to INFINITE to indicate no time-out value. If the time-out expires, the last error is set to ERROR_TIMEOUT.


### -param Flags [in]

Reserved. Must be zero.


### -param Returned [out]

The number of handles in the array that are set.


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
The function failed. To get the error code, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

</td>
</tr>
</table>
 




## -remarks



Call this function in a loop until the function returns <b>FALSE</b> and the error code is ERROR_NO_MORE_ITEMS.

For each event that you retrieve, you can then call the <a href="https://msdn.microsoft.com/729cfd74-c158-463d-9247-ee2c75b259d4">EvtCreateRenderContext</a> and <a href="https://msdn.microsoft.com/521322b6-3424-4321-bcba-fa8dcdc05a76">EvtRender</a> functions to render the event.

You must call <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> on each event handle that you receive.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/929bedbf-6dce-428e-b2c0-de9dcfe4531b">Querying for Events</a> and <a href="https://msdn.microsoft.com/1e86deeb-fc59-4658-9353-e4ced7ace89a">Subscribing to Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a>



<a href="https://msdn.microsoft.com/62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c">EvtSeek</a>



<a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a>
 

 


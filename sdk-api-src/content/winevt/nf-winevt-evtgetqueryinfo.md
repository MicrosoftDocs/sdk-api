---
UID: NF:winevt.EvtGetQueryInfo
title: EvtGetQueryInfo function
author: windows-sdk-content
description: Gets information about a query that you ran that identifies the list of channels or log files that the query attempted to access. The function also gets a list of return codes that indicates the success or failure of each access.
old-location: wes\evtgetqueryinfo.htm
tech.root: wes
ms.assetid: 311a2060-90d9-41ec-b489-c07d3e813187
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EvtGetQueryInfo, EvtGetQueryInfo function [EventLog], wes.evtgetqueryinfo, winevt/EvtGetQueryInfo
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
 - EvtGetQueryInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtGetQueryInfo function


## -description


Gets information about a query that you ran that identifies the list of channels or log files that the query attempted to access. The function also gets a list of return codes that indicates the success or failure of each access.


## -parameters




### -param QueryOrSubscription [in]

 A handle to the query that the<a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a> or  <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> function returns.


### -param PropertyId [in]

The identifier of the query information to retrieve. For a list of identifiers, see the <a href="https://msdn.microsoft.com/69a17378-088e-42e7-b7da-0ccc642f44d1">EVT_QUERY_PROPERTY_ID</a> enumeration.


### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.


### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the query information. The buffer contains an <a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.


### -param PropertyValueBufferUsed [out]

The size, in bytes, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.


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



You only need to call this function, if you pass the EvtQueryTolerateQueryErrors flag to <a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a> or the EvtSubscribeTolerateQueryErrors flag to <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a>.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/929bedbf-6dce-428e-b2c0-de9dcfe4531b">Querying for Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a>



<a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a>
 

 


---
UID: NF:winevt.EvtGetEventInfo
title: EvtGetEventInfo function (winevt.h)
author: windows-sdk-content
description: Gets information that identifies the structured XML query that selected the event and the channel or log file that contained the event.
old-location: wes\evtgeteventinfo.htm
tech.root: wes
ms.assetid: 69aa22a1-10c1-43bd-ae3b-d7641bed2065
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EvtGetEventInfo, EvtGetEventInfo function [EventLog], wes.evtgeteventinfo, winevt/EvtGetEventInfo
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
 - EvtGetEventInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtGetEventInfo function


## -description


Gets information that identifies the structured XML query that selected the event and the channel or log file that contained the event.


## -parameters




### -param Event [in]

A handle to an event for which you want to retrieve information.


### -param PropertyId [in]

A flag that identifies the information to retrieve. For example, the query identifier or the path. For possible values, see the <a href="https://msdn.microsoft.com/19e20da3-5b6b-4f56-b30b-0408695f2267">EVT_EVENT_PROPERTY_ID</a> enumeration.


### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.


### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the information. The buffer contains an <a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.


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
The function failed. Use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.

</td>
</tr>
</table>
 




## -remarks



If the query that you passed to <a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a> or <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> was an XPath instead of a structured XML query, the query identifier will be zero and the path will be the path that you passed to the function.




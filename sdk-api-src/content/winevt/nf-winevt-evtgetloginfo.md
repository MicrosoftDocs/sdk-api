---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EvtGetLogInfo function


## -description


Gets information about a channel or log file.


## -parameters




### -param Log [in]

 A handle to the channel or log file that the <a href="https://msdn.microsoft.com/1bf81452-2a62-4999-91b1-f1b42e6db91f">EvtOpenLog</a> function returns.


### -param PropertyId [in]

The identifier of the property to retrieve. For a list of property identifiers, see the <a href="https://msdn.microsoft.com/c5b8b80b-6549-497a-adc3-2517bd5f27c7">EVT_LOG_PROPERTY_ID</a> enumeration.


### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.


### -param PropertyValueBuffer [in]


A caller-allocated buffer that will receive the property value. The buffer contains an <a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.


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



 You can get complete information for Operational and Admin channels or .evtx files; however, for Debug and Analytic channels or .etl files, you cannot get information for the EvtLogFull, EvtLogOldestRecordNumber, and EvtLogNumberOfLogRecords properties.




## -see-also




<a href="https://msdn.microsoft.com/1bf81452-2a62-4999-91b1-f1b42e6db91f">EvtOpenLog</a>
 

 


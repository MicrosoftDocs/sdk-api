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

# IMpeg2Stream::SupplyDataBuffer


## -description



The <b>SupplyDataBuffer</b> method provides a buffer for the <b>Mpeg2Stream</b> object to write data.




## -parameters




### -param pStreamBuffer [in]

Pointer to an <a href="https://msdn.microsoft.com/d376af4c-4b22-4a2d-917a-6f25d2c38861">MPEG_STREAM_BUFFER</a> structure allocated by the caller. This structure contains a pointer to the buffer, also allocated by the caller. The buffer must be at least 4096 bytes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument or <b>NULL</b> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
</table>
 




## -remarks



The first time this method is called, it starts a worker thread that streams data to the buffer. When the data arrives, the <b>MPEG2Stream</b> object signals the event that was passed to the <a href="https://msdn.microsoft.com/a2ef2ebc-55dc-49d4-a5de-18203de113ce">IMpeg2Stream::Initialize</a> method. (Typically an application specifies the event handle when it calls <a href="https://msdn.microsoft.com/896080ff-cdf0-40b1-ba4e-d94de527d86e">IMpeg2Data::GetStreamOfSections</a>.)

When the event is signaled, examine the <b>hr</b> field of the <b>MPEG_STREAM_BUFFER</b> structure. If this value is a success code, the request was successful and the buffer contains valid data. To get more data, call the <b>SupplyDataBuffer</b> method again and wait for the event to be signaled.

The section headers are not converted from network byte order or otherwise processed.

If the object is still waiting for data, this method returns E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/189c921a-ec49-48dc-8c60-3d3ec2a648ca">IMpeg2Stream Interface</a>
 

 


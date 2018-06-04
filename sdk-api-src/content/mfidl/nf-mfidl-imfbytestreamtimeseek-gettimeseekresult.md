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

# IMFByteStreamTimeSeek::GetTimeSeekResult


## -description


Gets the result of a time-based seek.


## -parameters




### -param pqwStartTime [out]

Receives the new position after the seek, in 100-nanosecond units.


### -param pqwStopTime [out]

Receives the stop time, in 100-nanosecond units. If the stop time is unknown, the value is zero.


### -param pqwDuration [out]

Receives the total duration of the file, in 100-nanosecond units. If the duration is unknown, the value is –1.


## -returns



This method can return one of these values.

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The byte stream does not support time-based seeking, or no data is available.

</td>
</tr>
</table>
 




## -remarks



This method returns the server response from a previous time-based seek. 

<div class="alert"><b>Note</b>  This method normally cannot be invoked until some data
    is read from the byte stream, because the <a href="https://msdn.microsoft.com/786F1299-A9E2-4B2C-A6AE-F88E6BF022DC">IMFByteStreamTimeSeek::TimeSeek</a>       method does not send a server request immediately.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/BD9EDFF7-46BA-4788-A44E-C69C4B0BEB50">IMFByteStreamTimeSeek</a>
 

 


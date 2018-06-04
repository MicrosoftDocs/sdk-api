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

# IStreamBufferRecordControl::Start


## -description


The <b>Start</b> method starts the recording.


## -parameters




### -param prtStart [in, out]

Pointer to a variable that contains the start time. The time is relative to the current stream time, in 100-nanosecond units. The value zero represents now; negative values are in the past; and positive values are in the future.

For content recordings, the time must be a value between 0 and 5 seconds (50000000), inclusive. Negative times are not valid.

For reference recordings, negative times are valid if they fall within existing content. If the time given in <i>prtStart</i> is earlier than the earliest valid content, the actual start time of the content is used instead. This value is returned in <i>prtStart</i> when the method returns.


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
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
</table>
 




## -remarks



The start time must be less than or equal to the stop time.




## -see-also




<a href="https://msdn.microsoft.com/f196638e-ccbb-4768-96c1-8e1d00361831">IStreamBufferRecordControl Interface</a>



<a href="https://msdn.microsoft.com/1b6a3ac4-076a-4fca-909c-6063637248a8">IStreamBufferRecordControl::Stop</a>
 

 


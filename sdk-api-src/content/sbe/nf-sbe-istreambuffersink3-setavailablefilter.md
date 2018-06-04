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

# IStreamBufferSink3::SetAvailableFilter


## -description


The <b>SetAvailableFilter</b> method limits how far the Stream Buffer Source filter can seek backward, relative to the current recording position.


## -parameters




### -param prtMin [in, out]

On input, specifies the earliest seek time, in 100-nanosecond units, relative to the recording position when the method is called. The value must be less than or equal to zero. To make the entire backing store available, use the value -MAXLONGLONG.

On output, this parameter receives the actual minimum seek time. The two values may differ if the requested time exceeds the amount of time that is available.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -remarks



The minimum seek time is an absolute position within the file. For example, suppose the value is -50000000. Immediately after the method returns, the Stream Buffer Source filter can seek backward 5 seconds, but no further. After another 15 seconds of recording, the filter can seek backward 20 seconds from the new position.




## -see-also




<a href="https://msdn.microsoft.com/a3adbe79-7d7c-4b12-a574-23c64d2311af">IStreamBufferSink3 Interface</a>
 

 


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

# IMFASFMutualExclusion::GetStreamsForRecord


## -description



Retrieves the stream numbers contained in a record in the Advanced Systems Format mutual exclusion object.




## -parameters




### -param dwRecordNumber [in]

The number of the record for which to retrieve the stream numbers.


### -param pwStreamNumArray [out]

An array that receives the stream numbers. Set to <b>NULL</b> to get the number of elements required, which is indicated by the value of <i>pcStreams</i> on return. If this parameter is not <b>NULL</b>, the method will copy as many stream numbers to the array as there are elements indicated by the value of <i>pcStreams</i>.


### -param pcStreams [in, out]

On input, the number of elements in the array referenced by <i>pwStreamNumArray</i>. On output, the method sets this value to the count of stream numbers in the record. You can call <b>GetStreamsForRecord</b> with <i>pwStreamNumArray</i> set to <b>NULL</b> to retrieve the number of elements required to hold all of the stream numbers.


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
 




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 


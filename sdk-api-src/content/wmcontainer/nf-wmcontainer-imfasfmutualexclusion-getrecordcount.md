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

# IMFASFMutualExclusion::GetRecordCount


## -description



Retrieves the number of records in the Advanced Systems Format mutual exclusion object.




## -parameters




### -param pdwRecordCount [out]

Receives the count of records.


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



Each record includes one or more streams. Every stream in a record is mutually exclusive of streams in every other record.

Use this method in conjunction with <a href="https://msdn.microsoft.com/ce410ae9-d0d0-4617-8178-829ef3c77ce0">IMFASFMutualExclusion::GetStreamsForRecord</a> to retrieve the streams that are included in each record.




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/f5dedc87-a29c-4c8d-b493-486d975f9ac4">IMFASFMutualExclusion::AddRecord</a>



<a href="https://msdn.microsoft.com/ce410ae9-d0d0-4617-8178-829ef3c77ce0">IMFASFMutualExclusion::GetStreamsForRecord</a>



<a href="https://msdn.microsoft.com/ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8">IMFASFMutualExclusion::RemoveRecord</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 


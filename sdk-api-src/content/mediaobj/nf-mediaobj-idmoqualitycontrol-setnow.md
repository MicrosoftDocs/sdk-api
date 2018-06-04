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

# IDMOQualityControl::SetNow


## -description



The <code>SetNow</code> method specifies the earliest time stamp that the DMO will deliver.




## -parameters




### -param rtNow [in]

Reference time specifying the earliest time stamp to deliver.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



If quality control is enabled, the DMO discards any samples whose time stamp is less than <i>rtNow</i>. Samples whose time stamp is <i>rtNow</i> or later are processed as efficiently as possible. Depending on the implementation, the DMO might drop some samples to keep pace.

If quality control is disabled, this method has no immediate effect. However, the DMO stores the specified reference time. It uses this value if quality control is enabled at a later time. To enable quality control, call the <a href="https://msdn.microsoft.com/d22a7a23-6623-4a98-9a0c-5195b29781f9">IDMOQualityControl::SetStatus</a> method.

If incoming samples are not time-stamped, the DMO never performs quality control. The application sets the time stamp in the <a href="https://msdn.microsoft.com/f52e9586-f65d-418f-8c1a-c97c0a81d253">IMediaObject::ProcessInput</a> method.




## -see-also




<a href="https://msdn.microsoft.com/c23211f2-d4ba-45ff-b443-3425c3a3e72f">IDMOQualityControl Interface</a>
 

 


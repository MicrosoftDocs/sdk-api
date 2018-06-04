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

# IBackgroundCopyJob::GetType


## -description


Retrieves the type of transfer being performed, such as a file download or upload.


## -parameters




### -param pVal






#### - pJobType [out]

Type of transfer being performed. For a list of transfer types, see the 
<a href="https://msdn.microsoft.com/b341a63f-3a1d-4518-8f05-17d28af603b4">BG_JOB_TYPE</a> enumeration.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Transfer type was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pJobType</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Specify the type of transfer when you 
<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">create the job</a>.




## -see-also




<a href="https://msdn.microsoft.com/b341a63f-3a1d-4518-8f05-17d28af603b4">BG_JOB_TYPE</a>



<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">IBackgroundCopyManager::CreateJob</a>
 

 


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

# IBackgroundCopyJob::GetNoProgressTimeout


## -description


Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs. If there is progress, the timer is reset.


## -parameters




### -param Seconds






#### - pRetryPeriod [in]

Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.


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
Time-out was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Must pass the address of <i>pRetryPeriod</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/af599174-44f8-4d5e-b9ff-61ddbb330580">IBackgroundCopyJob::GetMinimumRetryDelay</a>



<a href="https://msdn.microsoft.com/3fcf46ed-197f-46ad-ac62-2c4a2e8b27ef">IBackgroundCopyJob::SetNoProgressTimeout</a>
 

 


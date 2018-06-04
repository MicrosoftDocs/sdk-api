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

# IBackgroundCopyJob::SetPriority


## -description


Specifies the priority level of your job. The priority level determines when your job is processed relative to other jobs in the transfer queue.


## -parameters




### -param Val






#### - Priority [in]

Specifies the priority level of your job relative to other jobs in the transfer queue. The default is BG_JOB_PRIORITY_NORMAL. For a list of priority levels, see the 
<a href="https://msdn.microsoft.com/bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e">BG_JOB_PRIORITY</a> enumeration.


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
Job priority was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>Priority</i> is not defined in the 
<a href="https://msdn.microsoft.com/bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e">BG_JOB_PRIORITY</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bfeab3bb-69bf-4ea2-a0ab-8f886c0d082e">BG_JOB_PRIORITY</a>



<a href="https://msdn.microsoft.com/8602ed59-a372-4cb3-bbda-cf1c7afc3669">IBackgroundCopyJob::GetPriority</a>
 

 


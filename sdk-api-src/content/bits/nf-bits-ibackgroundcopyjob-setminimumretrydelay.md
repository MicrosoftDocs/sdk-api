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

# IBackgroundCopyJob::SetMinimumRetryDelay


## -description


Sets the minimum length of time that BITS waits after encountering a transient error condition before trying to transfer the file.


## -parameters




### -param Seconds






#### - RetryDelay [in]

Minimum length of time, in seconds, that BITS waits after encountering a transient error before trying to transfer the file. The default retry delay is 600 seconds (10 minutes). The minimum retry delay that you can specify is 5 seconds. If you specify a value less than 5 seconds, BITS changes the value to 5 seconds. If the value exceeds the no-progress-timeout 
value retrieved from the <a href="https://msdn.microsoft.com/30aae990-1cc1-468b-9e5f-7ef5ce6eeb9a">GetNoProgressTimeout</a> method, BITS will not retry the transfer and moves the job to the BG_JOB_STATE_ERROR state.


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
Retry delay was successfully set.

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
 




## -remarks



To start the job before the minimum retry period expires, call the <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a>  method.

BITS does not retry the job if a network disconnect or disk lock error occurred (for example, chkdsk is running) or the <a href="https://msdn.microsoft.com/32c7e2b1-bac2-4708-a30c-f6b2a816c1a4">MaxInternetBandwidth</a> Group Policy is zero. 

<b>Note</b>  Changing the system clock does not affect the minimum retry delay. For example, if the current time is 2:00 P.M. and BITS is to retry the job at 2:10 P.M.,  moving the system clock forward ten or more minutes does not mean BITS  will retry the job  early—BITS will still retry the job in ten minutes. To reflect the system clock change in BITS, you must restart the computer or the BITS service.




## -see-also




<a href="https://msdn.microsoft.com/af599174-44f8-4d5e-b9ff-61ddbb330580">IBackgroundCopyJob::GetMinimumRetryDelay</a>



<a href="https://msdn.microsoft.com/4881e5f7-a835-40d5-a056-d6b23e3cd84c">IBackgroundCopyJob::GetNoProgressTimeout</a>



<a href="https://msdn.microsoft.com/3fcf46ed-197f-46ad-ac62-2c4a2e8b27ef">IBackgroundCopyJob::SetNoProgressTimeout</a>
 

 


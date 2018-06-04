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

# IBackgroundCopyJob4::SetMaximumDownloadTime


## -description


Sets the maximum time that BITS will spend transferring the files in the job.


## -parameters




### -param Timeout [in]

Maximum time, in seconds, that BITS will spend transferring the files in the job. The default is 7,776,000 seconds (90 days).


## -returns



The method returns the following return values.

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
Success

</td>
</tr>
</table>
 




## -remarks



The value is the maximum elapsed time that the job can spend in the CONNECTING or TRANSFERRING state. Time spent in the QUEUED or TRANSIENT_ERROR state does not count against the timeout value. The job enters the fatal error state with an error code of BG_E_MAXDOWNLOAD_TIMEOUT if the transfer time exceeds the timeout value. 

Note that if the computer sleeps while BITS is transferring the job's data, the time spent sleeping will count against the timeout even though data is not being transferred.

Calling the <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> method, resets the elapsed time.

This method overrides the MaxDownloadTime group policy.




## -see-also




<a href="https://msdn.microsoft.com/68909710-f749-487e-b064-9f8630929c53">IBackgroundCopyJob4</a>



<a href="https://msdn.microsoft.com/2d258dc4-a6fd-46d7-ac90-2703c8ddc666">IBackgroundCopyJob4::GetMaximumDownloadTime</a>
 

 


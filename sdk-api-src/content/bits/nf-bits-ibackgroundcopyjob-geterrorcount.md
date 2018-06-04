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

# IBackgroundCopyJob::GetErrorCount


## -description


Retrieves the number of times BITS tried to transfer the job and an error occurred.


## -parameters




### -param Errors






#### - pErrors [out]

Number of errors that occurred while BITS tried to transfer the job. The count increases  when the job moves from the BG_JOB_STATE_TRANSFERRING state to the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state. 


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -remarks



The count is never reset. The count may not accurately reflect the number of times the job moves to the transient error or error state. For example, BITS does not increase the count when network disconnects occur, the check disk program runs, or the bandwidth policy prevents jobs from transferring. 

BITS also increases the count each time it tries to transfer the job when the job is in the transient error state and the job fails.

<b>BITS 1.5 and earlier:  </b> BITS does not increase the count each time it tries to transfer the job when it is in the transient error state.




## -see-also




<a href="https://msdn.microsoft.com/2ad4c913-2d1e-4490-968c-960178a57e3b">IBackgroundCopyJob::GetError</a>
 

 


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

# IBackgroundCopyCallback::JobModification


## -description


BITS calls your implementation of the 
<b>JobModification</b> method when the job has been modified. The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.


## -parameters




### -param pJob [in]

Contains the methods for accessing property, progress, and state information of the job. Do not release <i>pJob</i>; BITS releases the interface when the <b>JobModification</b> method returns.


### -param dwReserved [in]

Reserved for future use.


## -returns



This method should return <b>S_OK</b>.




## -remarks



Your implementation may not receive all modification events under maximum resource load conditions.

BITS generates a high volume of modification events; consider creating a timer and polling for state and progress information or limiting your use of this callback. If you use this callback, keep your implementation short.

BITS does not generate a modify event when the state of the job changes to BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSFERRED.

<div class="alert"><b>Note</b>  BITS supports up to four simultaneous notifications per user. If one or more applications  block all four notifications for a user from returning, an application running as the same user will not receive  notifications until one or more of the blocking notifications return. </div>
<div> </div>

#### Examples

See the example code for the 
<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a> interface.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e1aa6775-d1e5-4463-ae0f-32c0498881e1">IBackgroundCopyCallback</a>



<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>
 

 


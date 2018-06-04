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

# PCLUSAPI_CLUS_WORKER_TERMINATE callback function


## -description


Terminates a worker thread. The <b>PCLUSAPI_CLUS_WORKER_TERMINATE</b> type defines a pointer to this function.


## -parameters




### -param lpWorker [in]

Pointer to a <a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a> structure describing the 
       thread to terminate.


## -returns



This function has no return values.




## -remarks



The <i>ClusWorkerTerminate</i> utility function checks 
     the <b>hThread</b> and <b>Terminate</b> members of the 
     <a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a> structure pointed to by 
     <i>lpWorker</i>. If <b>hThread</b> is not <b>NULL</b> 
     and <b>Terminate</b> is set to <b>FALSE</b>, indicating that this is your 
     first call to <i>ClusWorkerTerminate</i>, the function 
     waits for the thread to exit before returning. Otherwise, if you have called 
     <i>ClusWorkerTerminate</i> previously, indicated by 
     <b>Terminate</b> being set to <b>TRUE</b>, the function may return before 
     the thread has terminated.




## -see-also




<a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a>



<a href="https://msdn.microsoft.com/e8833961-ac0e-4d8c-a57e-5aabdb2c8c96">ClusWorkerCheckTerminate</a>



<a href="https://msdn.microsoft.com/a7e8f8ad-c9de-4c6b-8926-b9a46d85924d">ClusWorkerCreate</a>



<a href="https://msdn.microsoft.com/e2dda7c0-01d4-49e5-bc57-3fa07495d536">ClusWorkerTerminateEx</a>



<a href="https://msdn.microsoft.com/af9bcdcf-ca92-438b-94f2-f0e7529952fb">ClusWorkersTerminate</a>



<a href="https://msdn.microsoft.com/47436aab-a513-423b-8287-e467954e1dc1">Thread Management Utility Functions</a>
 

 


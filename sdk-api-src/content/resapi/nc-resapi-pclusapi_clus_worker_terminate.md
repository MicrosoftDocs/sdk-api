---
UID: NC:resapi.PCLUSAPI_CLUS_WORKER_TERMINATE
title: PCLUSAPI_CLUS_WORKER_TERMINATE
author: windows-sdk-content
description: Terminates a worker thread. The PCLUSAPI_CLUS_WORKER_TERMINATE type defines a pointer to this function.
old-location: mscs\clusworkerterminate.htm
tech.root: MsCS
ms.assetid: d143a860-92fe-4fa9-b0d7-d591376a0209
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: PCLUSAPI_CLUS_WORKER_TERMINATE, PCLUSAPI_CLUS_WORKER_TERMINATE callback, PCLUSAPI_CLUS_WORKER_TERMINATE callback function [Failover Cluster], _wolf_clusworkerterminate, mscs.clusworkerterminate, resapi/PCLUSAPI_CLUS_WORKER_TERMINATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PCLUSAPI_CLUS_WORKER_TERMINATE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 


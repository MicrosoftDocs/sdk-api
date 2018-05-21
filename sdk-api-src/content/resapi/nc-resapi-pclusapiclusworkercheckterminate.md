---
UID: NC:resapi.PCLUSAPIClusWorkerCheckTerminate
title: PCLUSAPIClusWorkerCheckTerminate
author: windows-driver-content
description: Determines whether a worker thread should exit as soon as possible. The PCLUSAPIClusWorkerCheckTerminate type defines a pointer to this function.
old-location: mscs\clusworkercheckterminate.htm
old-project: MsCS
ms.assetid: e8833961-ac0e-4d8c-a57e-5aabdb2c8c96
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PCLUSAPIClusWorkerCheckTerminate, PCLUSAPIClusWorkerCheckTerminate callback, PCLUSAPIClusWorkerCheckTerminate callback function [Failover Cluster], _wolf_clusworkercheckterminate, mscs.clusworkercheckterminate, resapi/PCLUSAPIClusWorkerCheckTerminate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PCLUSAPIClusWorkerCheckTerminate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PCLUSAPIClusWorkerCheckTerminate callback function


## -description


Determines whether a worker thread should exit as soon as possible. The <b>PCLUSAPIClusWorkerCheckTerminate</b> type defines a pointer to this function.


## -parameters




### -param lpWorker [in]

Pointer to a <a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a> structure describing the 
       thread to check.


## -returns



<i>ClusWorkerCheckTerminate</i> returns one of 
       the following values.




## -remarks



The <i>ClusWorkerCheckTerminate</i> utility 
     function checks the <b>Terminate</b> member of the 
     <a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a> structure to determine whether the thread 
     pointed to by Worker should exit. The <b>Terminate</b> member is used to prevent problems from occurring when multiple threads call 
     <a href="https://msdn.microsoft.com/d143a860-92fe-4fa9-b0d7-d591376a0209">ClusWorkerTerminate</a> on the same worker thread.




## -see-also




<a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a>



<a href="https://msdn.microsoft.com/a7e8f8ad-c9de-4c6b-8926-b9a46d85924d">ClusWorkerCreate</a>



<a href="https://msdn.microsoft.com/d143a860-92fe-4fa9-b0d7-d591376a0209">ClusWorkerTerminate</a>



<a href="https://msdn.microsoft.com/47436aab-a513-423b-8287-e467954e1dc1">Thread Management Utility Functions</a>
 

 


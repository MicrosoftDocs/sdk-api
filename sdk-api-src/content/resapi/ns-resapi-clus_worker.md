---
UID: NS:resapi.CLUS_WORKER
title: CLUS_WORKER
author: windows-driver-content
description: Contains information about a worker thread.
old-location: mscs\clus_worker.htm
old-project: MsCS
ms.assetid: 559b147f-8e8a-4bc7-94ea-e2042f288b6d
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PCLUS_WORKER, CLUS_WORKER, CLUS_WORKER structure [Failover Cluster], PCLUS_WORKER, PCLUS_WORKER structure pointer [Failover Cluster], _wolf_clus_worker, mscs.clus_worker, resapi/CLUS_WORKER, resapi/PCLUS_WORKER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CLUS_WORKER, *PCLUS_WORKER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ResApi.h
api_name:
-	CLUS_WORKER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CLUS_WORKER structure


## -description


Contains information about a worker thread.


## -struct-fields




### -field hThread

Handle to the worker thread.


### -field Terminate

Flag that indicates whether the thread is to be terminated.


## -remarks



A worker thread is a thread that is created to offload work from a main thread so that the main thread is not blocked.

A  <b>CLUS_WORKER</b> structure is returned as output from  <a href="https://msdn.microsoft.com/a7e8f8ad-c9de-4c6b-8926-b9a46d85924d">ClusWorkerCreate</a> and passed as input to  <a href="https://msdn.microsoft.com/e8833961-ac0e-4d8c-a57e-5aabdb2c8c96">ClusWorkerCheckTerminate</a> and  <a href="https://msdn.microsoft.com/d143a860-92fe-4fa9-b0d7-d591376a0209">ClusWorkerTerminate</a>. There is never any reason for an application or  <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> to alter the members of a  <b>CLUS_WORKER</b> structure. This structure should always be treated as read-only.

The 
<b>Terminate</b> member prevents a potential race condition that can occur if multiple threads call the  <a href="https://msdn.microsoft.com/d143a860-92fe-4fa9-b0d7-d591376a0209">ClusWorkerTerminate</a> function to end the same worker thread. The first call sets 
<b>Terminate</b> to <b>TRUE</b>. Subsequent calls return immediately after checking the value of 
<b>Terminate</b> without waiting for the thread to exit.




## -see-also




<a href="https://msdn.microsoft.com/e8833961-ac0e-4d8c-a57e-5aabdb2c8c96">ClusWorkerCheckTerminate</a>



<a href="https://msdn.microsoft.com/a7e8f8ad-c9de-4c6b-8926-b9a46d85924d">ClusWorkerCreate</a>



<a href="https://msdn.microsoft.com/d143a860-92fe-4fa9-b0d7-d591376a0209">ClusWorkerTerminate</a>
 

 


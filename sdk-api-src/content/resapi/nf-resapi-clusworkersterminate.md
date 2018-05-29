---
UID: NF:resapi.ClusWorkersTerminate
title: ClusWorkersTerminate function
author: windows-sdk-content
description: Waits for multiple worker threads to terminate up to the specified timeout.
old-location: mscs\clusworkersterminate.htm
old-project: MsCS
ms.assetid: af9bcdcf-ca92-438b-94f2-f0e7529952fb
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusWorkersTerminate, ClusWorkersTerminate function [Failover Cluster], mscs.clusworkersterminate, resapi/ClusWorkersTerminate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RESOURCE_EXIT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ResUtils.dll
api_name:
-	ClusWorkersTerminate
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ClusWorkersTerminate function


## -description


Waits for multiple  worker threads to terminate up to the specified timeout.  Optionally,  signals the threads to terminate at the end of the timeout.


## -parameters




### -param ClusWorkers [in, out]

Pointer to an array of <a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a> structures describing the 
       threads to terminate.


### -param ClusWorkersCount [in]

The number of structures in the <i>ClusWorkers</i> parameter.


### -param TimeoutInMilliseconds [in]

The timeout in milliseconds.


### -param WaitOnly [in]

If set <b>TRUE</b>, the function will return  at the end of the timeout; otherwise it will signal the threads to terminate and return.


## -returns



Returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> on failure.




## -see-also




<a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a>



<a href="https://msdn.microsoft.com/e8833961-ac0e-4d8c-a57e-5aabdb2c8c96">ClusWorkerCheckTerminate</a>



<a href="https://msdn.microsoft.com/a7e8f8ad-c9de-4c6b-8926-b9a46d85924d">ClusWorkerCreate</a>



<a href="https://msdn.microsoft.com/d143a860-92fe-4fa9-b0d7-d591376a0209">ClusWorkerTerminate</a>



<a href="https://msdn.microsoft.com/e2dda7c0-01d4-49e5-bc57-3fa07495d536">ClusWorkerTerminateEx</a>



<a href="https://msdn.microsoft.com/47436aab-a513-423b-8287-e467954e1dc1">Thread Management Utility Functions</a>
 

 


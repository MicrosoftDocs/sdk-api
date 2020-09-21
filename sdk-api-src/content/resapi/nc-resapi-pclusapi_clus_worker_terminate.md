---
UID: NC:resapi.PCLUSAPI_CLUS_WORKER_TERMINATE
title: PCLUSAPI_CLUS_WORKER_TERMINATE (resapi.h)
description: Terminates a worker thread. The PCLUSAPI_CLUS_WORKER_TERMINATE type defines a pointer to this function.
helpviewer_keywords: ["PCLUSAPI_CLUS_WORKER_TERMINATE","PCLUSAPI_CLUS_WORKER_TERMINATE callback","PCLUSAPI_CLUS_WORKER_TERMINATE callback function [Failover Cluster]","_wolf_clusworkerterminate","mscs.clusworkerterminate","resapi/PCLUSAPI_CLUS_WORKER_TERMINATE"]
old-location: mscs\clusworkerterminate.htm
tech.root: MsCS
ms.assetid: d143a860-92fe-4fa9-b0d7-d591376a0209
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_CLUS_WORKER_TERMINATE, PCLUSAPI_CLUS_WORKER_TERMINATE callback, PCLUSAPI_CLUS_WORKER_TERMINATE callback function [Failover Cluster], _wolf_clusworkerterminate, mscs.clusworkerterminate, resapi/PCLUSAPI_CLUS_WORKER_TERMINATE
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PCLUSAPI_CLUS_WORKER_TERMINATE
 - resapi/PCLUSAPI_CLUS_WORKER_TERMINATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PCLUSAPI_CLUS_WORKER_TERMINATE
---

# PCLUSAPI_CLUS_WORKER_TERMINATE callback function


## -description

Terminates a worker thread. The <b>PCLUSAPI_CLUS_WORKER_TERMINATE</b> type defines a pointer to this function.

## -parameters

### -param lpWorker [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a> structure describing the 
       thread to terminate.

## -remarks

The <i>ClusWorkerTerminate</i> utility function checks 
     the <b>hThread</b> and <b>Terminate</b> members of the 
     <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a> structure pointed to by 
     <i>lpWorker</i>. If <b>hThread</b> is not <b>NULL</b> 
     and <b>Terminate</b> is set to <b>FALSE</b>, indicating that this is your 
     first call to <i>ClusWorkerTerminate</i>, the function 
     waits for the thread to exit before returning. Otherwise, if you have called 
     <i>ClusWorkerTerminate</i> previously, indicated by 
     <b>Terminate</b> being set to <b>TRUE</b>, the function may return before 
     the thread has terminated.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercheckterminate">ClusWorkerCheckTerminate</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercreate">ClusWorkerCreate</a>



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-clusworkerterminateex">ClusWorkerTerminateEx</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkersterminate">ClusWorkersTerminate</a>



<a href="/previous-versions/windows/desktop/mscs/thread-management-utility-functions">Thread Management Utility Functions</a>
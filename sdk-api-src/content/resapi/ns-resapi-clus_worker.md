---
UID: NS:resapi.CLUS_WORKER
title: CLUS_WORKER (resapi.h)
description: Contains information about a worker thread.
helpviewer_keywords: ["*PCLUS_WORKER","CLUS_WORKER","CLUS_WORKER structure [Failover Cluster]","PCLUS_WORKER","PCLUS_WORKER structure pointer [Failover Cluster]","_wolf_clus_worker","mscs.clus_worker","resapi/CLUS_WORKER","resapi/PCLUS_WORKER"]
old-location: mscs\clus_worker.htm
tech.root: MsCS
ms.assetid: 559b147f-8e8a-4bc7-94ea-e2042f288b6d
ms.date: 12/05/2018
ms.keywords: '*PCLUS_WORKER, CLUS_WORKER, CLUS_WORKER structure [Failover Cluster], PCLUS_WORKER, PCLUS_WORKER structure pointer [Failover Cluster], _wolf_clus_worker, mscs.clus_worker, resapi/CLUS_WORKER, resapi/PCLUS_WORKER'
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
req.typenames: CLUS_WORKER, *PCLUS_WORKER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_WORKER
 - resapi/CLUS_WORKER
 - PCLUS_WORKER
 - resapi/PCLUS_WORKER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - CLUS_WORKER
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

A  <b>CLUS_WORKER</b> structure is returned as output from  <a href="/windows/desktop/api/resapi/nf-resapi-clusworkercreate">ClusWorkerCreate</a> and passed as input to  <a href="/windows/desktop/api/resapi/nf-resapi-clusworkercheckterminate">ClusWorkerCheckTerminate</a> and  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclusapi_clus_worker_terminate">ClusWorkerTerminate</a>. There is never any reason for an application or  <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> to alter the members of a  <b>CLUS_WORKER</b> structure. This structure should always be treated as read-only.

The 
<b>Terminate</b> member prevents a potential race condition that can occur if multiple threads call the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclusapi_clus_worker_terminate">ClusWorkerTerminate</a> function to end the same worker thread. The first call sets 
<b>Terminate</b> to <b>TRUE</b>. Subsequent calls return immediately after checking the value of 
<b>Terminate</b> without waiting for the thread to exit.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercheckterminate">ClusWorkerCheckTerminate</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercreate">ClusWorkerCreate</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkerterminate">ClusWorkerTerminate</a>
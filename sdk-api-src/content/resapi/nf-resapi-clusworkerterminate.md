---
UID: NF:resapi.ClusWorkerTerminate
title: ClusWorkerTerminate
description: Waits for a worker thread to terminate up to the specified timeout. (ClusWorkerTerminate)
helpviewer_keywords: ["ClusWorkerTerminate"]
ms.date: 07/01/2019
tech.root: MsCS
ms.keywords: ClusWorkerTerminate
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: resapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ClusWorkerTerminate
 - resapi/ClusWorkerTerminate
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - resutils.dll
api_name:
 - ClusWorkerTerminate
---

## -description

Terminates a worker thread. The [PCLUSAPI_CLUS_WORKER_TERMINATE](nc-resapi-pclusapi_clus_worker_terminate.md) type defines a pointer to this function.

## -parameters

### -param lpWorker

Pointer to a [CLUS_WORKER](ns-resapi-clus_worker.md) structure describing the thread to terminate.

## -remarks

This function has no return values.

The **ClusWorkerTerminate** utility function checks the *hThread* and *Terminate* members of the **CLUS_WORKER** structure pointed to by *lpWorker*. If *hThread* is not NULL and *Terminate* is set to FALSE, indicating that this is your first call to **ClusWorkerTerminate**, the function waits for the thread to exit before returning. Otherwise, if you have called **ClusWorkerTerminate** previously, indicated by *Terminate* being set to TRUE, the function may return before the thread has terminated.

## -see-also

[CLUS_WORKER](ns-resapi-clus_worker.md)
[ClusWorkerCreate](nf-resapi-clusworkercreate.md)
[ClusWorkerCheckTerminate](nf-resapi-clusworkercheckterminate.md)
[ClusWorkerTerminateEx](nf-resapi-clusworkerterminateex.md)
[ClusWorkersTerminate](nf-resapi-clusworkersterminate.md)


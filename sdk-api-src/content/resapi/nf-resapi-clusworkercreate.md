---
UID: NF:resapi.ClusWorkerCreate
title: ClusWorkerCreate function
author: windows-sdk-content
description: Creates a worker thread. The PCLUSAPI_CLUS_WORKER_CREATE type defines a pointer to this function.
old-location: mscs\clusworkercreate.htm
tech.root: MsCS
ms.assetid: a7e8f8ad-c9de-4c6b-8926-b9a46d85924d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusWorkerCreate, ClusWorkerCreate function [Failover Cluster], PCLUSAPI_CLUS_WORKER_CREATE, PCLUSAPI_CLUS_WORKER_CREATE function [Failover Cluster], _wolf_clusworkercreate, mscs.clusworkercreate, resapi/ClusWorkerCreate, resapi/PCLUSAPI_CLUS_WORKER_CREATE
ms.topic: function
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ClusWorkerCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusWorkerCreate function


## -description


Creates a worker thread. The <b>PCLUSAPI_CLUS_WORKER_CREATE</b> type defines a pointer to this function.


## -parameters




### -param lpWorker [out]

Pointer to a 
zero-initialized <a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a> structure that on return is filled in with a handle to the created thread and a flag that indicates whether the handle should be terminated. The caller should never need to refer to or change the members of this structure.


### -param lpStartAddress [in]

Pointer to the address of a function that should be called by the worker thread.


### -param lpParameter [in]

A parameter to pass to the function whose address is pointed to by <i>lpStartAddress</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a>



<a href="https://msdn.microsoft.com/e8833961-ac0e-4d8c-a57e-5aabdb2c8c96">ClusWorkerCheckTerminate</a>



<a href="https://msdn.microsoft.com/d143a860-92fe-4fa9-b0d7-d591376a0209">ClusWorkerTerminate</a>
 

 


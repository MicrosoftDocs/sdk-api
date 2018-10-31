---
UID: NC:resapi.PWORKER_START_ROUTINE
title: PWORKER_START_ROUTINE
author: windows-sdk-content
description: Initializes a worker thread with the specified callback routine. The PWORKER_START_ROUTINE type defines a pointer to this function.
old-location: mscs\pworker_start_routine.htm
tech.root: mscs
ms.assetid: d46eaaa7-241a-40a5-a691-68631565e2e7
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PWORKER_START_ROUTINE, PWORKER_START_ROUTINE callback function [Failover Cluster], WorkerStartRoutine, WorkerStartRoutine callback, WorkerStartRoutine callback function [Failover Cluster], mscs.pworker_start_routine, resapi/PWORKER_START_ROUTINE, resapi/WorkerStartRoutine
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - WorkerStartRoutine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWORKER_START_ROUTINE callback function


## -description


Initializes a worker thread with the specified callback routine. The <b>PWORKER_START_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param pWorker [in]

A pointer to the <a href="https://msdn.microsoft.com/559b147f-8e8a-4bc7-94ea-e2042f288b6d">CLUS_WORKER</a> structure that represents the worker thread.


### -param lpThreadParameter [in]

A pointer to the callback routine to use to initialize the worker thread.


## -returns



Returns <b>ERROR_SUCCESS</b> (0), if the operation succeeds; otherwise returns a system error code.




## -remarks



The pointer to this  callback function is used as an input parameter for the <a href="https://msdn.microsoft.com/a7e8f8ad-c9de-4c6b-8926-b9a46d85924d">ClusWorkerCreate</a> function.




## -see-also




<a href="https://msdn.microsoft.com/a7e8f8ad-c9de-4c6b-8926-b9a46d85924d">ClusWorkerCreate</a>



<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 


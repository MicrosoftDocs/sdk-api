---
UID: NC:resapi.PWORKER_START_ROUTINE
title: PWORKER_START_ROUTINE (resapi.h)
description: Initializes a worker thread with the specified callback routine. The PWORKER_START_ROUTINE type defines a pointer to this function.
helpviewer_keywords: ["PWORKER_START_ROUTINE","PWORKER_START_ROUTINE callback function [Failover Cluster]","WorkerStartRoutine","WorkerStartRoutine callback","WorkerStartRoutine callback function [Failover Cluster]","mscs.pworker_start_routine","resapi/PWORKER_START_ROUTINE","resapi/WorkerStartRoutine"]
old-location: mscs\pworker_start_routine.htm
tech.root: MsCS
ms.assetid: d46eaaa7-241a-40a5-a691-68631565e2e7
ms.date: 12/05/2018
ms.keywords: PWORKER_START_ROUTINE, PWORKER_START_ROUTINE callback function [Failover Cluster], WorkerStartRoutine, WorkerStartRoutine callback, WorkerStartRoutine callback function [Failover Cluster], mscs.pworker_start_routine, resapi/PWORKER_START_ROUTINE, resapi/WorkerStartRoutine
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWORKER_START_ROUTINE
 - resapi/PWORKER_START_ROUTINE
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
 - WorkerStartRoutine
---

# PWORKER_START_ROUTINE callback function


## -description

Initializes a worker thread with the specified callback routine. The <b>PWORKER_START_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param pWorker [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a> structure that represents the worker thread.

### -param lpThreadParameter [in]

A pointer to the callback routine to use to initialize the worker thread.

## -returns

Returns <b>ERROR_SUCCESS</b> (0), if the operation succeeds; otherwise returns a system error code.

## -remarks

The pointer to this  callback function is used as an input parameter for the <a href="/windows/desktop/api/resapi/nf-resapi-clusworkercreate">ClusWorkerCreate</a> function.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercreate">ClusWorkerCreate</a>



<a href="/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>
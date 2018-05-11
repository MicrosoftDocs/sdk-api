---
UID: NC:clusapi.PCLUSTER_REG_CLOSE_BATCH
title: PCLUSTER_REG_CLOSE_BATCH
author: windows-driver-content
description: Executes or ignores the batch created by the ClusterRegCreateBatch function.
old-location: mscs\clusterregclosebatch.htm
old-project: MsCS
ms.assetid: d43644cf-370b-499f-b321-24e43f145a98
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PCLUSTER_REG_CLOSE_BATCH, PCLUSTER_REG_CLOSE_BATCH callback, PCLUSTER_REG_CLOSE_BATCH callback function [Failover Cluster], clusapi/PCLUSTER_REG_CLOSE_BATCH, mscs.clusterregclosebatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSTER_REG_CLOSE_BATCH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSTER_REG_CLOSE_BATCH callback function


## -description


Executes or ignores the batch created by the 
    <a href="https://msdn.microsoft.com/83e7c216-f08f-4dc2-9b53-faa2760985d4">ClusterRegCreateBatch</a> function.


## -parameters




### -param hRegBatch [in]

The handle of the  cluster registry key opened by 
       <a href="https://msdn.microsoft.com/83e7c216-f08f-4dc2-9b53-faa2760985d4">ClusterRegCreateBatch</a>. After the completion 
       of <i>ClusterRegCloseBatch</i>, this handle is no 
       longer valid and memory associated with it is freed.


### -param bCommit [in]

If the value this parameter takes is true, then a batch is sent for execution to a cluster server.


### -param *failedCommandNumber [out, optional]

If execution of the batch is not successful, the number of the command that failed is returned in the form of 
       a <i>failedCommandNumber</i> argument. The first command in the batch has number 0, the 
       second has number 1, and so on.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



If a failure has occurred before any command was executed, the <i>failedCommandNumber</i> 
     parameter is set to –1.

The <b>PCLUSTER_REG_CLOSE_BATCH</b> type defines a pointer to this function.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/3d59e68a-deb3-443f-9d8f-281cdb15e8b6">ClusterRegBatchAddCommand</a>



<a href="https://msdn.microsoft.com/127d06de-28a4-4df4-9f5f-17ea4a330528">ClusterRegCloseBatchEx</a>



<a href="https://msdn.microsoft.com/83e7c216-f08f-4dc2-9b53-faa2760985d4">ClusterRegCreateBatch</a>
 

 


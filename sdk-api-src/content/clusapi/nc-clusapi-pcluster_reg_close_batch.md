---
UID: NC:clusapi.PCLUSTER_REG_CLOSE_BATCH
title: PCLUSTER_REG_CLOSE_BATCH
author: windows-sdk-content
description: Executes or ignores the batch created by the ClusterRegCreateBatch function.
old-location: mscs\clusterregclosebatch.htm
old-project: mscs
ms.assetid: d43644cf-370b-499f-b321-24e43f145a98
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSTER_REG_CLOSE_BATCH, PCLUSTER_REG_CLOSE_BATCH callback, PCLUSTER_REG_CLOSE_BATCH callback function [Failover Cluster], clusapi/PCLUSTER_REG_CLOSE_BATCH, mscs.clusterregclosebatch
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSTER_REG_CLOSE_BATCH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSTER_REG_CLOSE_BATCH callback function


## -description


Executes or ignores the batch created by the 
    <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a> function.


## -parameters




### -param hRegBatch [in]

The handle of the  cluster registry key opened by 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a>. After the completion 
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
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



If a failure has occurred before any command was executed, the <i>failedCommandNumber</i> 
     parameter is set to –1.

The <b>PCLUSTER_REG_CLOSE_BATCH</b> type defines a pointer to this function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369128(v=VS.85).aspx">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/3d59e68a-deb3-443f-9d8f-281cdb15e8b6">ClusterRegBatchAddCommand</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn806590(v=VS.85).aspx">ClusterRegCloseBatchEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a>
 

 


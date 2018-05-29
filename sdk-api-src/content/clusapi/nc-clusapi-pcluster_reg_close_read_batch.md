---
UID: NC:clusapi.PCLUSTER_REG_CLOSE_READ_BATCH
title: PCLUSTER_REG_CLOSE_READ_BATCH
author: windows-sdk-content
description: Executes a read batch and returns results from the read batch executions.
old-location: mscs\clusterregclosereadbatch.htm
old-project: MsCS
ms.assetid: A164EB9F-290E-446E-98E9-95C6C3C3D00C
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSTER_REG_CLOSE_READ_BATCH, PCLUSTER_REG_CLOSE_READ_BATCH callback, PCLUSTER_REG_CLOSE_READ_BATCH callback function [Failover Cluster], clusapi/PCLUSTER_REG_CLOSE_READ_BATCH, mscs.clusterregclosereadbatch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
-	PCLUSTER_REG_CLOSE_READ_BATCH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSTER_REG_CLOSE_READ_BATCH callback function


## -description


Executes a read batch and returns results from the read batch executions.


## -parameters




### -param hRegReadBatch [in]

The handle of the read batch. After the <i>ClusterRegCloseReadBatch</i> function completes, this handle is no longer valid, and memory associated with it is freed.


### -param *phRegReadBatchReply [out]

A pointer to the handle of the created read batch result. You must close this handle later by calling the  <a href="https://msdn.microsoft.com/C8CC4292-A7CC-4613-B5A8-B504E804E00E">ClusterRegCloseReadBatchReply</a> function.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



Create the read batch by calling the <a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a> function.




## -see-also




<a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a>



<a href="https://msdn.microsoft.com/2B665231-7325-43C4-92A4-4EDF28126BA1">ClusterRegReadBatchAddCommand</a>
 

 


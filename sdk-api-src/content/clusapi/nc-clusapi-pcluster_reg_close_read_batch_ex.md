---
UID: NC:clusapi.PCLUSTER_REG_CLOSE_READ_BATCH_EX
title: PCLUSTER_REG_CLOSE_READ_BATCH_EX
author: windows-driver-content
description: Executes a read batch and returns results from the read batch executions.
old-location: mscs\clusterregclosereadbatchex.htm
old-project: MsCS
ms.assetid: 45509B96-F67D-4754-B073-0B881D681011
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IsolatedRead, None, PCLUSTER_REG_CLOSE_READ_BATCH_EX, PCLUSTER_REG_CLOSE_READ_BATCH_EX callback, PCLUSTER_REG_CLOSE_READ_BATCH_EX callback function [Failover Cluster], clusapi/PCLUSTER_REG_CLOSE_READ_BATCH_EX, mscs.clusterregclosereadbatchex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSTER_REG_CLOSE_READ_BATCH_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSTER_REG_CLOSE_READ_BATCH_EX callback function


## -description


Executes a read batch and returns results from the read batch executions.


## -parameters




### -param hRegReadBatch [in]

The handle of the read batch. After the <a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a> function completes, this handle is no longer valid, and memory associated with it is freed.


### -param flags

The flags for the operation.



#### None (0)



#### IsolatedRead (2)


### -param *phRegReadBatchReply [out]

A pointer to the handle of the created read batch result. You must close this handle later by calling the  <a href="https://msdn.microsoft.com/C8CC4292-A7CC-4613-B5A8-B504E804E00E">ClusterRegCloseReadBatchReply</a> function.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a>



<a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a>



<a href="https://msdn.microsoft.com/2B665231-7325-43C4-92A4-4EDF28126BA1">ClusterRegReadBatchAddCommand</a>
 

 


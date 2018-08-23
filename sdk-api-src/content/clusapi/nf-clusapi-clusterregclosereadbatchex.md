---
UID: NF:clusapi.ClusterRegCloseReadBatchEx
title: ClusterRegCloseReadBatchEx function
author: windows-sdk-content
description: Executes a read batch and returns results from the read batch executions.
old-location: mscs\clusterregclosereadbatchex.htm
old-project: mscs
ms.assetid: 45509B96-F67D-4754-B073-0B881D681011
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusterRegCloseReadBatchEx, ClusterRegCloseReadBatchEx function [Failover Cluster], IsolatedRead, None, PCLUSTER_REG_CLOSE_READ_BATCH_EX, PCLUSTER_REG_CLOSE_READ_BATCH_EX function [Failover Cluster], clusapi/ClusterRegCloseReadBatchEx, clusapi/PCLUSTER_REG_CLOSE_READ_BATCH_EX, mscs.clusterregclosereadbatchex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterRegCloseReadBatchEx
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegCloseReadBatchEx function


## -description


Executes a read batch and returns results from the read batch executions.


## -parameters




### -param hRegReadBatch [in]

The handle of the read batch. After the <a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a> function completes, this handle is no longer valid, and memory associated with it is freed.


### -param flags

The flags for the operation.



#### None (0)



#### IsolatedRead (2)


### -param phRegReadBatchReply [out]

A pointer to the handle of the created read batch result. You must close this handle later by calling the  <a href="https://msdn.microsoft.com/en-us/library/Hh706742(v=VS.85).aspx">ClusterRegCloseReadBatchReply</a> function.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369128(v=VS.85).aspx">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706743(v=VS.85).aspx">ClusterRegCreateReadBatch</a>



<a href="https://msdn.microsoft.com/2B665231-7325-43C4-92A4-4EDF28126BA1">ClusterRegReadBatchAddCommand</a>
 

 


---
UID: NF:clusapi.ClusterRegCloseBatch
title: ClusterRegCloseBatch function
author: windows-sdk-content
description: Executes or ignores the batch created by the ClusterRegCreateBatch function.
old-location: mscs\clusterregclosebatch.htm
tech.root: mscs
ms.assetid: d43644cf-370b-499f-b321-24e43f145a98
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ClusterRegCloseBatch, ClusterRegCloseBatch function [Failover Cluster], PCLUSTER_REG_CLOSE_BATCH, PCLUSTER_REG_CLOSE_BATCH function [Failover Cluster], clusapi/ClusterRegCloseBatch, clusapi/PCLUSTER_REG_CLOSE_BATCH, mscs.clusterregclosebatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegCloseBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegCloseBatch function


## -description


Executes or ignores the batch created by the 
    <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a> function.


## -parameters




### -param hRegBatch [in]

The handle of the  cluster registry key opened by 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a>. After the completion 
       of <b>ClusterRegCloseBatch</b>, this handle is no 
       longer valid and memory associated with it is freed.


### -param bCommit [in]

If the value this parameter takes is true, then a batch is sent for execution to a cluster server.


### -param failedCommandNumber [out, optional]

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
 

 


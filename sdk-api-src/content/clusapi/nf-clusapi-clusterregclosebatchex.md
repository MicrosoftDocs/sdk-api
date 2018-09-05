---
UID: NF:clusapi.ClusterRegCloseBatchEx
title: ClusterRegCloseBatchEx function
author: windows-sdk-content
description: Executes or ignores the batch created by the ClusterRegCreateBatch function.
old-location: mscs\clusterregclosebatchex.htm
old-project: mscs
ms.assetid: 127d06de-28a4-4df4-9f5f-17ea4a330528
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ClusterRegCloseBatchEx, ClusterRegCloseBatchEx function [Failover Cluster], clusapi/ClusterRegCloseBatchEx, mscs.clusterregclosebatchex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegCloseBatchEx
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegCloseBatchEx function


## -description


Executes or ignores the batch created by the 
    <a href="https://msdn.microsoft.com/83e7c216-f08f-4dc2-9b53-faa2760985d4">ClusterRegCreateBatch</a> function.


## -parameters




### -param hRegBatch [in]

The handle of the  cluster registry key opened by 
       <a href="https://msdn.microsoft.com/83e7c216-f08f-4dc2-9b53-faa2760985d4">ClusterRegCreateBatch</a>. After the completion 
       of <a href="https://msdn.microsoft.com/d43644cf-370b-499f-b321-24e43f145a98">ClusterRegCloseBatch</a>, this handle is no 
       longer valid and memory associated with it is freed.


### -param flags [in]


### -param failedCommandNumber [out, optional]

If execution of the batch is not successful, the number of the command that failed is returned in the form of 
       a <i>failedCommandNumber</i> argument. The first command in the batch has number 0, the 
       second has number 1, and so on.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



If a failure has occurred before any command was executed, the <i>failedCommandNumber</i> 
     parameter is set to –1.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/d43644cf-370b-499f-b321-24e43f145a98">ClusterRegCloseBatch</a>
 

 


---
UID: NF:clusapi.ClusterRegCreateReadBatch
title: ClusterRegCreateReadBatch function
author: windows-sdk-content
description: Creates a handle to the read batch that executes read commands on the cluster registry key.
old-location: mscs\clusterregcreatereadbatch.htm
old-project: mscs
ms.assetid: FED3986E-7383-46C4-B2D5-259812EF63A2
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusterRegCreateReadBatch, ClusterRegCreateReadBatch function [Failover Cluster], clusapi/ClusterRegCreateReadBatch, mscs.clusterregcreatereadbatch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegCreateReadBatch
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegCreateReadBatch function


## -description


Creates a handle to the read batch that executes read commands on the cluster registry key.


## -parameters




### -param hKey [in]

The handle to the opened cluster registry key. All of the operations on the batch are relative to this cluster registry key.


### -param phRegReadBatch [out]

A pointer to the handle of the created read batch.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



Add commands to the batch by calling the <a href="https://msdn.microsoft.com/2B665231-7325-43C4-92A4-4EDF28126BA1">ClusterRegReadBatchAddCommand</a>  function. Execute the batch by calling the <a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a> function.

Do not close the key until the read batch has been submitted for execution.




## -see-also




<a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a>



<a href="https://msdn.microsoft.com/2B665231-7325-43C4-92A4-4EDF28126BA1">ClusterRegReadBatchAddCommand</a>
 

 


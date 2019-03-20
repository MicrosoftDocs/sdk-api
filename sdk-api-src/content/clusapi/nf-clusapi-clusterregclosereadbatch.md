---
UID: NF:clusapi.ClusterRegCloseReadBatch
title: ClusterRegCloseReadBatch function (clusapi.h)
author: windows-sdk-content
description: Executes a read batch and returns results from the read batch executions.
old-location: mscs\clusterregclosereadbatch.htm
tech.root: MsCS
ms.assetid: A164EB9F-290E-446E-98E9-95C6C3C3D00C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterRegCloseReadBatch, ClusterRegCloseReadBatch function [Failover Cluster], PCLUSTER_REG_CLOSE_READ_BATCH, PCLUSTER_REG_CLOSE_READ_BATCH function [Failover Cluster], clusapi/ClusterRegCloseReadBatch, clusapi/PCLUSTER_REG_CLOSE_READ_BATCH, mscs.clusterregclosereadbatch
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegCloseReadBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegCloseReadBatch function


## -description


Executes a read batch and returns results from the read batch executions.


## -parameters




### -param hRegReadBatch [in]

The handle of the read batch. After the <b>ClusterRegCloseReadBatch</b> function completes, this handle is no longer valid, and memory associated with it is freed.


### -param phRegReadBatchReply [out]

A pointer to the handle of the created read batch result. You must close this handle later by calling the  <a href="https://msdn.microsoft.com/C8CC4292-A7CC-4613-B5A8-B504E804E00E">ClusterRegCloseReadBatchReply</a> function.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
<i>hRegReadBatch</i> is <b>NULL</b> or not valid.

</td>
</tr>
</table>
 




## -remarks



Create the read batch by calling the <a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a> function.




## -see-also




<a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a>



<a href="https://msdn.microsoft.com/2B665231-7325-43C4-92A4-4EDF28126BA1">ClusterRegReadBatchAddCommand</a>
 

 


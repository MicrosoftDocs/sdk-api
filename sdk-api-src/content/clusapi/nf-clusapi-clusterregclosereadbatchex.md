---
UID: NF:clusapi.ClusterRegCloseReadBatchEx
title: ClusterRegCloseReadBatchEx function
author: windows-sdk-content
description: Executes a read batch and returns results from the read batch executions.
old-location: mscs\clusterregclosereadbatchex.htm
tech.root: MsCS
ms.assetid: 45509B96-F67D-4754-B073-0B881D681011
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterRegCloseReadBatchEx, ClusterRegCloseReadBatchEx function [Failover Cluster], IsolatedRead, None, PCLUSTER_REG_CLOSE_READ_BATCH_EX, PCLUSTER_REG_CLOSE_READ_BATCH_EX function [Failover Cluster], clusapi/ClusterRegCloseReadBatchEx, clusapi/PCLUSTER_REG_CLOSE_READ_BATCH_EX, mscs.clusterregclosereadbatchex
ms.topic: function
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
api_name:
 - ClusterRegCloseReadBatchEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a>



<a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a>



<a href="https://msdn.microsoft.com/2B665231-7325-43C4-92A4-4EDF28126BA1">ClusterRegReadBatchAddCommand</a>
 

 


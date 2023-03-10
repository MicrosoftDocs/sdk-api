---
UID: NF:clusapi.ClusterRegCloseReadBatchEx
title: ClusterRegCloseReadBatchEx function (clusapi.h)
description: Executes a read batch and returns results from the read batch executions. (ClusterRegCloseReadBatchEx)
helpviewer_keywords: ["ClusterRegCloseReadBatchEx","ClusterRegCloseReadBatchEx function [Failover Cluster]","IsolatedRead","None","PCLUSTER_REG_CLOSE_READ_BATCH_EX","PCLUSTER_REG_CLOSE_READ_BATCH_EX function [Failover Cluster]","clusapi/ClusterRegCloseReadBatchEx","clusapi/PCLUSTER_REG_CLOSE_READ_BATCH_EX","mscs.clusterregclosereadbatchex"]
old-location: mscs\clusterregclosereadbatchex.htm
tech.root: MsCS
ms.assetid: 45509B96-F67D-4754-B073-0B881D681011
ms.date: 12/05/2018
ms.keywords: ClusterRegCloseReadBatchEx, ClusterRegCloseReadBatchEx function [Failover Cluster], IsolatedRead, None, PCLUSTER_REG_CLOSE_READ_BATCH_EX, PCLUSTER_REG_CLOSE_READ_BATCH_EX function [Failover Cluster], clusapi/ClusterRegCloseReadBatchEx, clusapi/PCLUSTER_REG_CLOSE_READ_BATCH_EX, mscs.clusterregclosereadbatchex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterRegCloseReadBatchEx
 - clusapi/ClusterRegCloseReadBatchEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterRegCloseReadBatchEx
---

# ClusterRegCloseReadBatchEx function


## -description

Executes a read batch and returns results from the read batch executions.

## -parameters

### -param hRegReadBatch [in]

The handle of the read batch. After the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a> function completes, this handle is no longer valid, and memory associated with it is freed.

### -param flags

The flags for the operation.



#### None (0)



#### IsolatedRead (2)

### -param phRegReadBatchReply [out]

A pointer to the handle of the created read batch result. You must close this handle later by calling the  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatchreply">ClusterRegCloseReadBatchReply</a> function.

## -returns

The function returns one of the following 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

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

<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatereadbatch">ClusterRegCreateReadBatch</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregreadbatchaddcommand">ClusterRegReadBatchAddCommand</a>

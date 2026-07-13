---
UID: NF:clusapi.ClusterRegCloseReadBatch
title: ClusterRegCloseReadBatch function (clusapi.h)
description: Executes a read batch and returns results from the read batch executions. (ClusterRegCloseReadBatch)
helpviewer_keywords: ["ClusterRegCloseReadBatch","ClusterRegCloseReadBatch function [Failover Cluster]","PCLUSTER_REG_CLOSE_READ_BATCH","PCLUSTER_REG_CLOSE_READ_BATCH function [Failover Cluster]","clusapi/ClusterRegCloseReadBatch","clusapi/PCLUSTER_REG_CLOSE_READ_BATCH","mscs.clusterregclosereadbatch"]
old-location: mscs\clusterregclosereadbatch.htm
tech.root: MsCS
ms.assetid: A164EB9F-290E-446E-98E9-95C6C3C3D00C
ms.date: 12/05/2018
ms.keywords: ClusterRegCloseReadBatch, ClusterRegCloseReadBatch function [Failover Cluster], PCLUSTER_REG_CLOSE_READ_BATCH, PCLUSTER_REG_CLOSE_READ_BATCH function [Failover Cluster], clusapi/ClusterRegCloseReadBatch, clusapi/PCLUSTER_REG_CLOSE_READ_BATCH, mscs.clusterregclosereadbatch
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterRegCloseReadBatch
 - clusapi/ClusterRegCloseReadBatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegCloseReadBatch
---

# ClusterRegCloseReadBatch function


## -description

Executes a read batch and returns results from the read batch executions.

## -parameters

### -param hRegReadBatch [in]

The handle of the read batch. After the <b>ClusterRegCloseReadBatch</b> function completes, this handle is no longer valid, and memory associated with it is freed.

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

## -remarks

Create the read batch by calling the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatereadbatch">ClusterRegCreateReadBatch</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatereadbatch">ClusterRegCreateReadBatch</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregreadbatchaddcommand">ClusterRegReadBatchAddCommand</a>

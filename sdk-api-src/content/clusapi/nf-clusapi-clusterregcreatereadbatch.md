---
UID: NF:clusapi.ClusterRegCreateReadBatch
title: ClusterRegCreateReadBatch function (clusapi.h)
description: Creates a handle to the read batch that executes read commands on the cluster registry key.
helpviewer_keywords: ["ClusterRegCreateReadBatch","ClusterRegCreateReadBatch function [Failover Cluster]","clusapi/ClusterRegCreateReadBatch","mscs.clusterregcreatereadbatch"]
old-location: mscs\clusterregcreatereadbatch.htm
tech.root: MsCS
ms.assetid: FED3986E-7383-46C4-B2D5-259812EF63A2
ms.date: 12/05/2018
ms.keywords: ClusterRegCreateReadBatch, ClusterRegCreateReadBatch function [Failover Cluster], clusapi/ClusterRegCreateReadBatch, mscs.clusterregcreatereadbatch
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
 - ClusterRegCreateReadBatch
 - clusapi/ClusterRegCreateReadBatch
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
 - ClusterRegCreateReadBatch
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
</table>

## -remarks

Add commands to the batch by calling the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregreadbatchaddcommand">ClusterRegReadBatchAddCommand</a>  function. Execute the batch by calling the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a> function.

Do not close the key until the read batch has been submitted for execution.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregreadbatchaddcommand">ClusterRegReadBatchAddCommand</a>
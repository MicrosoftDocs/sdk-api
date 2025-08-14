---
UID: NF:clusapi.ClusterRegCreateBatch
title: ClusterRegCreateBatch function (clusapi.h)
description: Creates a batch that will execute commands on a cluster registry key.
helpviewer_keywords: ["ClusterRegCreateBatch","ClusterRegCreateBatch function [Failover Cluster]","PCLUSTER_REG_CREATE_BATCH","clusapi/ClusterRegCreateBatch","mscs.clusterregcreatebatch"]
old-location: mscs\clusterregcreatebatch.htm
tech.root: MsCS
ms.assetid: 83e7c216-f08f-4dc2-9b53-faa2760985d4
ms.date: 12/05/2018
ms.keywords: ClusterRegCreateBatch, ClusterRegCreateBatch function [Failover Cluster], PCLUSTER_REG_CREATE_BATCH, clusapi/ClusterRegCreateBatch, mscs.clusterregcreatebatch
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterRegCreateBatch
 - clusapi/ClusterRegCreateBatch
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegCreateBatch
---

# ClusterRegCreateBatch function


## -description

Creates a batch that will execute commands on a cluster registry key. These commands will 
    be added to the batch by the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregbatchaddcommand">ClusterRegBatchAddCommand</a> function and 
    either executed or ignored by the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosebatch">ClusterRegCloseBatch</a> function.

## -parameters

### -param hKey [in, optional]

The handle of the opened cluster registry key.  All the operations on the batch are relative to this cluster 
       registry key.

### -param pHREGBATCH [out]

The pointer to the handle of the created batch.

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
<dt>14 (0xE)</dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
<dt>31 (0x1F)</dt>
</dl>
</td>
<td width="60%">
A device attached to the system is not functioning.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87 (0x57)</dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. This value will be returned if the <i>hKey</i> parameter is 
         <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The key should not be closed until the batch has been submitted for execution.

The <b>PCLUSTER_REG_CREATE_BATCH</b> type defines a pointer to this function.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregbatchaddcommand">ClusterRegBatchAddCommand</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosebatch">ClusterRegCloseBatch</a>
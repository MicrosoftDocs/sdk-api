---
UID: NF:clusapi.ClusterRegReadBatchAddCommand
title: ClusterRegReadBatchAddCommand function (clusapi.h)
description: Adds a read command to a batch that executes on a cluster registry key.
helpviewer_keywords: ["ClusterRegReadBatchAddCommand","ClusterRegReadBatchAddCommand function [Failover Cluster]","clusapi/ClusterRegReadBatchAddCommand","mscs.clusterregreadbatchaddcommand"]
old-location: mscs\clusterregreadbatchaddcommand.htm
tech.root: MsCS
ms.assetid: 2B665231-7325-43C4-92A4-4EDF28126BA1
ms.date: 12/05/2018
ms.keywords: ClusterRegReadBatchAddCommand, ClusterRegReadBatchAddCommand function [Failover Cluster], clusapi/ClusterRegReadBatchAddCommand, mscs.clusterregreadbatchaddcommand
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
 - ClusterRegReadBatchAddCommand
 - clusapi/ClusterRegReadBatchAddCommand
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
 - ClusterRegReadBatchAddCommand
---

# ClusterRegReadBatchAddCommand function


## -description

Adds a read command to a batch that executes on a cluster registry key.

## -parameters

### -param hRegReadBatch [in]

The handle of the read batch to which a command will be added. Create a batch by calling the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatereadbatch">ClusterRegCreateReadBatch</a> function.

### -param wzSubkeyName [in, optional]

The name of the key relative to the cluster registry key. If this name is <b>NULL</b>, the read is performed on the cluster registry key represented in the <i>hRegReadBatch</i> parameter.

### -param wzValueName [in, optional]

The name of the registry value to be read. If this name is <b>NULL</b>, the content of the default value is returned.

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

Additional calls to the <b>ClusterRegReadBatchAddCommand</b> function add additional read commands to the batch.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatereadbatch">ClusterRegCreateReadBatch</a>
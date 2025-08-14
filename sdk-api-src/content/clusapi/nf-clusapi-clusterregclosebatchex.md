---
UID: NF:clusapi.ClusterRegCloseBatchEx
title: ClusterRegCloseBatchEx function (clusapi.h)
description: Executes or ignores the batch created by the ClusterRegCreateBatch function. (ClusterRegCloseBatchEx)
helpviewer_keywords: ["ClusterRegCloseBatchEx","ClusterRegCloseBatchEx function [Failover Cluster]","clusapi/ClusterRegCloseBatchEx","mscs.clusterregclosebatchex"]
old-location: mscs\clusterregclosebatchex.htm
tech.root: MsCS
ms.assetid: 127d06de-28a4-4df4-9f5f-17ea4a330528
ms.date: 12/05/2018
ms.keywords: ClusterRegCloseBatchEx, ClusterRegCloseBatchEx function [Failover Cluster], clusapi/ClusterRegCloseBatchEx, mscs.clusterregclosebatchex
req.header: clusapi.h
req.include-header: 
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterRegCloseBatchEx
 - clusapi/ClusterRegCloseBatchEx
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
 - ClusterRegCloseBatchEx
---

# ClusterRegCloseBatchEx function


## -description

Executes or ignores the batch created by the 
    <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatebatch">ClusterRegCreateBatch</a> function.

## -parameters

### -param hRegBatch [in]

The handle of the  cluster registry key opened by 
       <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatebatch">ClusterRegCreateBatch</a>. After the completion 
       of <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosebatch">ClusterRegCloseBatch</a>, this handle is no 
       longer valid and memory associated with it is freed.

### -param flags [in]

### -param failedCommandNumber [out, optional]

If execution of the batch is not successful, the number of the command that failed is returned in the form of 
       a <i>failedCommandNumber</i> argument. The first command in the batch has number 0, the 
       second has number 1, and so on.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The handle is not valid. This value is returned if the <i>hRegBatch</i> parameter 
        is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

If a failure has occurred before any command was executed, the <i>failedCommandNumber</i> 
     parameter is set to –1.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosebatch">ClusterRegCloseBatch</a>

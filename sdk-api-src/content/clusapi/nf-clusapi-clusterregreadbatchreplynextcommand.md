---
UID: NF:clusapi.ClusterRegReadBatchReplyNextCommand
title: ClusterRegReadBatchReplyNextCommand function (clusapi.h)
description: Reads the next command from a read batch result.
helpviewer_keywords: ["ClusterRegReadBatchReplyNextCommand","ClusterRegReadBatchReplyNextCommand function [Failover Cluster]","clusapi/ClusterRegReadBatchReplyNextCommand","mscs.clusterregreadbatchreplynextcommand"]
old-location: mscs\clusterregreadbatchreplynextcommand.htm
tech.root: MsCS
ms.assetid: 4E0DEB5C-36AA-480C-913C-235DE9AEA58D
ms.date: 12/05/2018
ms.keywords: ClusterRegReadBatchReplyNextCommand, ClusterRegReadBatchReplyNextCommand function [Failover Cluster], clusapi/ClusterRegReadBatchReplyNextCommand, mscs.clusterregreadbatchreplynextcommand
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
 - ClusterRegReadBatchReplyNextCommand
 - clusapi/ClusterRegReadBatchReplyNextCommand
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
 - ClusterRegReadBatchReplyNextCommand
---

# ClusterRegReadBatchReplyNextCommand function


## -description

Reads the next command from a read batch result.

## -parameters

### -param hRegReadBatchReply [in]

A handle to a read batch result that was created by calling the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a> function.  You must close this handle later by calling the  <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatchreply">ClusterRegCloseReadBatchReply</a> function.

### -param pBatchCommand [out]

A pointer to a <a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_read_batch_command">CLUSTER_READ_BATCH_COMMAND</a> structure that contains information about the read command.

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
<i>hRegReadBatchReply</i> is <b>NULL</b> or not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
<dt>259</dt>
</dl>
</td>
<td width="60%">
There is no more information in <i>hRegReadBatchReply</i>.

</td>
</tr>
</table>

## -remarks

The number of records in the read batch results is equal to the number of commands in the read batch. Also, the results are in the same order as the commands that were added to the read batch.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_read_batch_command">CLUSTER_READ_BATCH_COMMAND</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatchreply">ClusterRegCloseReadBatchReply</a>
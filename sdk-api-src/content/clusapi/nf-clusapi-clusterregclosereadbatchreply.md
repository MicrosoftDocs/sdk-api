---
UID: NF:clusapi.ClusterRegCloseReadBatchReply
title: ClusterRegCloseReadBatchReply function (clusapi.h)
description: Closes a read batch result handle and frees the memory associated with it.
helpviewer_keywords: ["ClusterRegCloseReadBatchReply","ClusterRegCloseReadBatchReply function [Failover Cluster]","clusapi/ClusterRegCloseReadBatchReply","mscs.clusterregclosereadbatchreply"]
old-location: mscs\clusterregclosereadbatchreply.htm
tech.root: MsCS
ms.assetid: C8CC4292-A7CC-4613-B5A8-B504E804E00E
ms.date: 12/05/2018
ms.keywords: ClusterRegCloseReadBatchReply, ClusterRegCloseReadBatchReply function [Failover Cluster], clusapi/ClusterRegCloseReadBatchReply, mscs.clusterregclosereadbatchreply
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
 - ClusterRegCloseReadBatchReply
 - clusapi/ClusterRegCloseReadBatchReply
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
 - ClusterRegCloseReadBatchReply
---

# ClusterRegCloseReadBatchReply function


## -description

Closes a read batch result handle and frees the memory associated with it.

## -parameters

### -param hRegReadBatchReply [in]

A handle to a read batch result that was created by calling the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a> function.

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
</table>

## -remarks

Call the <b>ClusterRegCloseReadBatchReply</b> function to close a read batch result that was created by the  <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a> function.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatch">ClusterRegCloseReadBatch</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregreadbatchreplynextcommand">ClusterRegReadBatchReplyNextCommand</a>
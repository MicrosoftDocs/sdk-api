---
UID: NF:clusapi.ClusterRegBatchCloseNotification
title: ClusterRegBatchCloseNotification function (clusapi.h)
description: Frees the memory associated with the batch notification.
helpviewer_keywords: ["ClusterRegBatchCloseNotification","ClusterRegBatchCloseNotification function [Failover Cluster]","PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION","clusapi/ClusterRegBatchCloseNotification","mscs.clusterregbatchclosenotification"]
old-location: mscs\clusterregbatchclosenotification.htm
tech.root: MsCS
ms.assetid: d7a127ba-6e97-46ac-8510-2da355359c50
ms.date: 12/05/2018
ms.keywords: ClusterRegBatchCloseNotification, ClusterRegBatchCloseNotification function [Failover Cluster], PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION, clusapi/ClusterRegBatchCloseNotification, mscs.clusterregbatchclosenotification
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
 - ClusterRegBatchCloseNotification
 - clusapi/ClusterRegBatchCloseNotification
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
 - ClusterRegBatchCloseNotification
---

# ClusterRegBatchCloseNotification function


## -description

Frees the memory associated with the batch notification.

## -parameters

### -param hBatchNotification [in]

A handle to the batch notification.

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
The operation was successful. This error returns if the command is properly filled.

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
The handle is not valid. This error is returned if the <i>hBatchNotification</i> 
         parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION</b> type defines a pointer to this 
     function.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>
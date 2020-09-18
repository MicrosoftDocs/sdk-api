---
UID: NF:clusapi.ClusterRegCreateBatchNotifyPort
title: ClusterRegCreateBatchNotifyPort function (clusapi.h)
description: Creates a subscription to a batch notification port.
helpviewer_keywords: ["ClusterRegCreateBatchNotifyPort","ClusterRegCreateBatchNotifyPort function [Failover Cluster]","PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT","clusapi/ClusterRegCreateBatchNotifyPort","mscs.clusterregcreatebatchnotifyport"]
old-location: mscs\clusterregcreatebatchnotifyport.htm
tech.root: MsCS
ms.assetid: 1eca2ba5-c0c3-4388-9384-db9dbcfc8405
ms.date: 12/05/2018
ms.keywords: ClusterRegCreateBatchNotifyPort, ClusterRegCreateBatchNotifyPort function [Failover Cluster], PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT, clusapi/ClusterRegCreateBatchNotifyPort, mscs.clusterregcreatebatchnotifyport
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
 - ClusterRegCreateBatchNotifyPort
 - clusapi/ClusterRegCreateBatchNotifyPort
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
 - ClusterRegCreateBatchNotifyPort
---

# ClusterRegCreateBatchNotifyPort function


## -description

Creates a subscription to a batch notification port. The batch notification port needs to 
    be closed after it is no longer needed. This is done via the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosebatchnotifyport">ClusterRegCloseBatchNotifyPort</a> 
    function.

## -parameters

### -param hKey [in]

A cluster registry key. Any updates performed at this key or keys below it will be posted to a notification 
       port.

### -param phBatchNotifyPort [out]

A handle to a batch notification port that allows subsequent reading batch notifications via the 
       <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterreggetbatchnotification">ClusterRegGetBatchNotification</a> 
       function.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <b>PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT</b> type defines a pointer to this 
     function.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregclosebatchnotifyport">ClusterRegCloseBatchNotifyPort</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterreggetbatchnotification">ClusterRegGetBatchNotification</a>
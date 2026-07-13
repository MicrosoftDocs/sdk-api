---
UID: NF:clusapi.DestroyCluster
title: DestroyCluster function (clusapi.h)
description: Removes a cluster.
helpviewer_keywords: ["DestroyCluster","DestroyCluster function [Failover Cluster]","PCLUSAPI_DESTROY_CLUSTER","PCLUSAPI_DESTROY_CLUSTER function [Failover Cluster]","clusapi/DestroyCluster","clusapi/PCLUSAPI_DESTROY_CLUSTER","mscs.destroycluster"]
old-location: mscs\destroycluster.htm
tech.root: MsCS
ms.assetid: 55e601de-b427-43cd-b7f8-6cc576077e59
ms.date: 12/05/2018
ms.keywords: DestroyCluster, DestroyCluster function [Failover Cluster], PCLUSAPI_DESTROY_CLUSTER, PCLUSAPI_DESTROY_CLUSTER function [Failover Cluster], clusapi/DestroyCluster, clusapi/PCLUSAPI_DESTROY_CLUSTER, mscs.destroycluster
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
 - DestroyCluster
 - clusapi/DestroyCluster
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
 - DestroyCluster
---

# DestroyCluster function


## -description

Removes a cluster. The <b>PCLUSAPI_DESTROY_CLUSTER</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to a cluster, returned by the <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a> or 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a> function.

### -param pfnProgressCallback [in, optional]

Address of callback function that matches the 
      <a href="/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">PCLUSTER_SETUP_PROGRESS_CALLBACK</a> 
      function pointer that will be called periodically to provide progress on the cluster destruction.

### -param pvCallbackArg [in, optional]

Argument for the callback function.

### -param fdeleteVirtualComputerObjects [in]

If <b>TRUE</b>, then delete the virtual computer objects associated with the cluster 
      from the directory.

## -returns

Returns <b>ERROR_SUCCESS</b> if the cluster was completely removed or a 
      <a href="/windows/desktop/Debug/system-error-codes">system error code</a> for the last failed operation.

## -remarks

It is possible for multiple steps to fail when removing a cluster with 
    <b>DestroyCluster</b>, but only one error code can be 
    returned. The cluster error log should be reviewed if an error is returned.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Cluster Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>
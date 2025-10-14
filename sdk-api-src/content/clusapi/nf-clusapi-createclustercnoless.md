---
UID: NF:clusapi.CreateClusterCNOless
title: CreateClusterCNOless function (clusapi.h)
description: Creates a cluster without cluster name and IP Address resources.
helpviewer_keywords: ["CreateClusterCNOless","CreateClusterCNOless function [Failover Cluster]","PCLUSAPI_CREATE_CLUSTER_CNOLESS","PCLUSAPI_CREATE_CLUSTER_CNOLESS function [Failover Cluster]","clusapi/CreateClusterCNOless","clusapi/PCLUSAPI_CREATE_CLUSTER_CNOLESS","mscs.createclustercnoless"]
old-location: mscs\createclustercnoless.htm
tech.root: MsCS
ms.assetid: AED4CDC5-BE90-4F34-A8E2-DFD0617BC65B
ms.date: 12/05/2018
ms.keywords: CreateClusterCNOless, CreateClusterCNOless function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_CNOLESS, PCLUSAPI_CREATE_CLUSTER_CNOLESS function [Failover Cluster], clusapi/CreateClusterCNOless, clusapi/PCLUSAPI_CREATE_CLUSTER_CNOLESS, mscs.createclustercnoless
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - CreateClusterCNOless
 - clusapi/CreateClusterCNOless
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
 - CreateClusterCNOless
---

# CreateClusterCNOless function


## -description

Creates a cluster without <a href="/previous-versions/windows/desktop/mscs/network-name">cluster name</a> and <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a>  resources. The allows you to create clusters that are domain joined but not managed by Active Directory, and clusters that are not members of a domain. <b>PCLUSAPI_CREATE_CLUSTER_CNOLESS</b> defines a pointer to this function.

## -parameters

### -param pConfig [in]

A pointer to the <a href="/windows/desktop/api/clusapi/ns-clusapi-create_cluster_config">CREATE_CLUSTER_CONFIG</a> structure that contains the cluster configuration.

### -param pfnProgressCallback [in, optional]

A pointer to the <a href="/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">ClusterSetupProgressCallback</a> callback function that receives the status of updates to the cluster.

### -param pvCallbackArg [in, optional]

Callback function arguments for the <i>pfnProgressCallback</i> parameter.

## -returns

A handle to the new cluster or <b>NULL</b>. A non <b>NULL</b> 
      value does not indicate success (even if all nodes are added to the cluster, the <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a> or 
      <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resource creation can fail). After a failure, you should check the parameters 
      passed through the   <i>pfnProgressCallback</i> parameter.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
Less than a majority of nodes were successfully created. For more information about the error, call the 
        function <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -remarks

To create clusters that are not domain joined, a non-domain account must have permission to manage the cluster remotely.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Functions</a>
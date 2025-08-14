---
UID: NF:clusapi.CreateCluster
title: CreateCluster function (clusapi.h)
description: Creates and starts a cluster.
helpviewer_keywords: ["CreateCluster","CreateCluster function [Failover Cluster]","PCLUSAPI_CREATE_CLUSTER","PCLUSAPI_CREATE_CLUSTER function [Failover Cluster]","clusapi/CreateCluster","clusapi/PCLUSAPI_CREATE_CLUSTER","mscs.createcluster"]
old-location: mscs\createcluster.htm
tech.root: MsCS
ms.assetid: 672a1573-63e5-4321-a049-25bdafc1b5e0
ms.date: 12/05/2018
ms.keywords: CreateCluster, CreateCluster function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER, PCLUSAPI_CREATE_CLUSTER function [Failover Cluster], clusapi/CreateCluster, clusapi/PCLUSAPI_CREATE_CLUSTER, mscs.createcluster
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
 - CreateCluster
 - clusapi/CreateCluster
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
 - CreateCluster
---

# CreateCluster function


## -description

Creates and starts a cluster. The cluster consists of the set of nodes specified, with the 
    <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a>, 
    <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a>, and 
    <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resources</a> if specified. The <b>PCLUSAPI_CREATE_CLUSTER</b> type defines a pointer to this function.

## -parameters

### -param pConfig [in]

Address of a <a href="/windows/desktop/api/clusapi/ns-clusapi-create_cluster_config">CREATE_CLUSTER_CONFIG</a> 
      structure containing configuration information about the cluster to be created.

### -param pfnProgressCallback [in, optional]

Address of callback function that matches the 
      <a href="/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">PCLUSTER_SETUP_PROGRESS_CALLBACK</a> 
      function pointer that will be called periodically to provide progress on the cluster creation.

### -param pvCallbackArg [in, optional]

Argument for the callback function.

## -returns

Handle to the newly created cluster or <b>NULL</b>. A non <b>NULL</b> 
      value does not indicate complete success (all nodes will have been added, but not all 
      <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a> or 
      <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resources may have been created. The parameters 
      passed to the function pointed to by the <i>pfnProgressCallback</i> parameter should be 
      checked.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>NULL</b></b></dt>
</dl>
</td>
<td width="60%">
Less than a majority of nodes were successfully created. For more information about the error, call the 
        function <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -remarks

The <b>PCLUSAPI_CREATE_CLUSTER</b> type defines a pointer to this function and can be 
    used with the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to call this 
    function.

After the <b>CreateCluster</b> function successfully 
    completes, at least 30 seconds should be allowed before the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-addclusternode">AddClusterNode</a> function is called to add additional 
    nodes.

The <b>CreateCluster</b> function successfully completes 
    after cluster quorum has been achieved. One or more cluster nodes could be in a 
    <b>ClusterNodeDown</b> or <b>ClusterNodeJoining</b> state for a few 
    seconds.

Before calling the <b>CreateCluster</b> function, 
    the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> function must be called specifying 
    both <b>COINIT_MULTITHREADED</b> and <b>COINIT_DISABLE_OLE1DDE</b> for 
    the <i>dwCoInit</i> parameter, as shown in the following code.


``` syntax
CoInitializeEx( NULL, COINIT_MULTITHREADED | COINIT_DISABLE_OLE1DDE );
```


## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-addclusternode">AddClusterNode</a>



<a href="/windows/desktop/api/clusapi/ns-clusapi-create_cluster_config">CREATE_CLUSTER_CONFIG</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Cluster Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-destroycluster">DestroyCluster</a>



<a href="/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>

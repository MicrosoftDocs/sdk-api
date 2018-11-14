---
UID: NF:clusapi.OpenCluster
title: OpenCluster function
author: windows-sdk-content
description: Opens a connection to a cluster and returns a handle to it.
old-location: mscs\opencluster.htm
tech.root: mscs
ms.assetid: b2ee2575-cc1e-4696-8e95-9798fb556c58
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: OpenCluster, OpenCluster function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER, PCLUSAPI_OPEN_CLUSTER function [Failover Cluster], _wolf_opencluster, clusapi/OpenCluster, clusapi/PCLUSAPI_OPEN_CLUSTER, mscs.opencluster
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - OpenCluster
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OpenCluster
: 
---

# OpenCluster function


## -description


Opens a connection to a 
    <a href="c_gly.htm">cluster</a> and returns a handle to 
    it.


## -parameters




### -param lpszClusterName [in, optional]

Specifies one of the following values:

<ul>
<li>Pointer to a null-terminated Unicode string containing the name of the cluster or one of the cluster 
        <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> expressed as a NetBIOS name, a fully qualified DNS name, or 
        an IP address. This produces an RPC cluster handle.</li>
<li><b>NULL</b>, which produces an LPC handle to the cluster to which the local computer 
        belongs.</li>
</ul>

## -returns



If the operation was successful, <b>OpenCluster</b> returns 
       a cluster handle.




## -remarks



A cluster handle is a pointer to an internally defined structure which stores information about the RPC or LPC 
     connection to the cluster. Any object handles obtained from the cluster handle will be associated with the RPC or 
     LPC session data stored in the cluster structure. Combining RPC and LPC handles or using handles obtained from 
     different contexts can cause exceptions or other unpredictable results. For more information, see 
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a>.

When finished with a cluster handle, it is important to call 
     <a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a> to ensure that all memory is freed and the 
     connection is shut down cleanly.

If the cluster is remote, the client must be running a compatible operating system. For example computers running 
     Windows Server 2008 cannot call <b>OpenCluster</b> against a 
     cluster running Windows Server 2016. To remotely manage these clusters, use 
     <a href="mscs.the_server_cluster_wmi_provider">the Failover Cluster WMI Provider</a>.


#### Examples

See <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Functions</a>



<a href="https://msdn.microsoft.com/688702b7-7525-48d6-9e44-d7c4969565f8">OpenClusterEx</a>
 

 


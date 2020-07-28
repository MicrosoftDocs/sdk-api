---
UID: NF:clusapi.AddClusterNode
title: AddClusterNode function (clusapi.h)
description: Adds a node to an existing cluster.
helpviewer_keywords: ["AddClusterNode","AddClusterNode function [Failover Cluster]","PCLUSAPI_ADD_CLUSTER_NODE","PCLUSAPI_ADD_CLUSTER_NODE function [Failover Cluster]","clusapi/AddClusterNode","clusapi/PCLUSAPI_ADD_CLUSTER_NODE","mscs.addclusternode"]
old-location: mscs\addclusternode.htm
tech.root: MsCS
ms.assetid: e1d3611e-10d1-4858-923a-01633d2ed78b
ms.date: 12/05/2018
ms.keywords: AddClusterNode, AddClusterNode function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_NODE, PCLUSAPI_ADD_CLUSTER_NODE function [Failover Cluster], clusapi/AddClusterNode, clusapi/PCLUSAPI_ADD_CLUSTER_NODE, mscs.addclusternode
f1_keywords:
- clusapi/AddClusterNode
dev_langs:
- c++
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
- AddClusterNode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AddClusterNode function


## -description


Adds a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a> to an existing cluster. The <b>PCLUSAPI_ADD_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster, returned by the <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a> or 
       <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a> function.


### -param lpszNodeName [in]

Name of the computer to add to the cluster.


### -param pfnProgressCallback [in, optional]

Optional address to a 
       <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">PCLUSTER_SETUP_PROGRESS_CALLBACK</a> 
       callback function.


### -param pvCallbackArg [in, optional]

Argument for the callback function.


## -returns



Handle to the new node or <b>NULL</b> to indicate that the node was not successfully added 
       to the cluster. For more information about the error, call the 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -remarks



After the <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a> function successfully 
     completes, at least 30 seconds should be allowed before the 
     <b>AddClusterNode</b> function is called to add additional 
     nodes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nc-clusapi-pcluster_setup_progress_callback">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>
 

 


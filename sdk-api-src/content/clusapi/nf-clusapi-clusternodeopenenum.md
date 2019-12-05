---
UID: NF:clusapi.ClusterNodeOpenEnum
title: ClusterNodeOpenEnum function (clusapi.h)
description: Opens an enumerator for iterating through the network interfaces or groups installed on a node.
old-location: mscs\clusternodeopenenum.htm
tech.root: MsCS
ms.assetid: f187f4d7-24c8-477d-91fc-0ef738b66f22
ms.date: 12/05/2018
ms.keywords: CLUSTER_NODE_ENUM_ALL, CLUSTER_NODE_ENUM_GROUPS, CLUSTER_NODE_ENUM_NETINTERFACES, ClusterNodeOpenEnum, ClusterNodeOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_OPEN_ENUM, PCLUSAPI_CLUSTER_NODE_OPEN_ENUM function [Failover Cluster], _wolf_clusternodeopenenum, clusapi/ClusterNodeOpenEnum, clusapi/PCLUSAPI_CLUSTER_NODE_OPEN_ENUM, mscs.clusternodeopenenum
ms.topic: function
f1_keywords:
- clusapi/ClusterNodeOpenEnum
dev_langs:
- c++
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
api_name:
- ClusterNodeOpenEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterNodeOpenEnum function


## -description


Opens an 
    enumerator for iterating through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/network-interfaces">network interfaces</a>  
    or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/groups">groups</a> installed on a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a>. The <b>PCLUSAPI_CLUSTER_NODE_OPEN_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to a node.


### -param dwType [in]

Bitmask describing the type of objects to be enumerated. The following values of the 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_node_enum">CLUSTER_NODE_ENUM</a> enumeration are valid.



#### CLUSTER_NODE_ENUM_NETINTERFACES (0x00000001)

Enumerate the network interface objects on the node.



#### CLUSTER_NODE_ENUM_GROUPS (0x00000002)

Enumerate the cluster groups on the node.



#### CLUSTER_NODE_ENUM_ALL ((CLUSTER_NODE_ENUM_NETINTERFACES | CLUSTER_NODE_ENUM_GROUPS))

Enumerate the network interfaces objects and cluster groups on the node.

<b>Windows Server 2008:  </b>The <b>CLUSTER_NODE_ENUM_GROUPS</b> value is not supported before 
          Windows Server 2008 R2.


## -returns



If the operation succeeds, 
       <b>ClusterNodeOpenEnum</b> returns a handle to a node 
       enumerator.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -remarks



The <b>ClusterNodeOpenEnum</b> function returns a 
     handle that can be passed to <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeenum">ClusterNodeEnum</a> to 
     access each of the objects to be enumerated and to 
     <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodecloseenum">ClusterNodeCloseEnum</a> to release the 
     enumerator.


#### Examples

See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_node_enum">CLUSTER_NODE_ENUM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodecloseenum">ClusterNodeCloseEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeenum">ClusterNodeEnum</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>
 

 


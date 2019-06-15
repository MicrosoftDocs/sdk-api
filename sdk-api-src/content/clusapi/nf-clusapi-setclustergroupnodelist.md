---
UID: NF:clusapi.SetClusterGroupNodeList
title: SetClusterGroupNodeList function (clusapi.h)
author: windows-sdk-content
description: Sets the preferred node list for a group.
old-location: mscs\setclustergroupnodelist.htm
tech.root: MsCS
ms.assetid: 663ccafe-0456-406e-a50d-e17e6d85a9a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_GROUP_NODE_LIST, PCLUSAPI_SET_CLUSTER_GROUP_NODE_LIST function [Failover Cluster], SetClusterGroupNodeList, SetClusterGroupNodeList function [Failover Cluster], _wolf_setclustergroupnodelist, clusapi/PCLUSAPI_SET_CLUSTER_GROUP_NODE_LIST, clusapi/SetClusterGroupNodeList, mscs.setclustergroupnodelist
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
api_name:
 - SetClusterGroupNodeList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetClusterGroupNodeList function


## -description


Sets the preferred  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a> list for a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/groups">group</a>. The <b>PCLUSAPI_SET_CLUSTER_GROUP_NODE_LIST</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to be assigned the list of nodes.


### -param NodeCount [in]

Count of nodes in the list identified by <i>NodeList</i>.


### -param NodeList [in]

Array of handles to nodes, in order by preference, with the first node being the most preferred and the last node the least preferred. The number of nodes in the <i>NodeList</i> array is controlled by the <i>NodeCount</i> parameter.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -remarks



Do not call  <b>SetClusterGroupNodeList</b> from a resource DLL. For more information, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and  <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>
 

 


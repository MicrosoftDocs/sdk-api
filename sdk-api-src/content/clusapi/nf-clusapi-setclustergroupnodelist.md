---
UID: NF:clusapi.SetClusterGroupNodeList
title: SetClusterGroupNodeList function
author: windows-sdk-content
description: Sets the preferred node list for a group.
old-location: mscs\setclustergroupnodelist.htm
tech.root: mscs
ms.assetid: 663ccafe-0456-406e-a50d-e17e6d85a9a1
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_GROUP_NODE_LIST, PCLUSAPI_SET_CLUSTER_GROUP_NODE_LIST function [Failover Cluster], SetClusterGroupNodeList, SetClusterGroupNodeList function [Failover Cluster], _wolf_setclustergroupnodelist, clusapi/PCLUSAPI_SET_CLUSTER_GROUP_NODE_LIST, clusapi/SetClusterGroupNodeList, mscs.setclustergroupnodelist
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
api_name:
 - SetClusterGroupNodeList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClusterGroupNodeList function


## -description


Sets the preferred  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> list for a  <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a>. The <b>PCLUSAPI_SET_CLUSTER_GROUP_NODE_LIST</b> type defines a pointer to this function.


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
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Do not call  <b>SetClusterGroupNodeList</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and  <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 


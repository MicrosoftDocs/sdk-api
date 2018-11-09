---
UID: NF:clusapi.OpenClusterNode
title: OpenClusterNode function
author: windows-sdk-content
description: Opens a node and returns a handle to it.
old-location: mscs\openclusternode.htm
tech.root: mscs
ms.assetid: 7658a030-d4b2-407c-829f-61491b5907e6
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: OpenClusterNode, OpenClusterNode function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NODE, PCLUSAPI_OPEN_CLUSTER_NODE function [Failover Cluster], _wolf_openclusternode, clusapi/OpenClusterNode, clusapi/PCLUSAPI_OPEN_CLUSTER_NODE, mscs.openclusternode
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
 - OpenClusterNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenClusterNode function


## -description


Opens a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> and returns a handle to it. The <b>PCLUSAPI_OPEN_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a <a href="c_gly.htm">cluster</a> returned from the 
      <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a> or 
      <a href="https://msdn.microsoft.com/688702b7-7525-48d6-9e44-d7c4969565f8">OpenClusterEx</a> functions.


### -param lpszNodeName [in]

Pointer to the NetBIOS name of an existing node. If the DNS name of the node is used, the 
      <b>OpenClusterNode</b> function will fail and 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return 
      <b>ERROR_CLUSTER_NODE_NOT_FOUND</b>.


## -returns



If the operation was successful, <b>OpenClusterNode</b> 
       returns a node handle.




## -see-also




<a href="https://msdn.microsoft.com/e2d90b7e-d181-48b6-a891-b885c24a15ea">CloseClusterNode</a>



<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/688702b7-7525-48d6-9e44-d7c4969565f8">OpenClusterEx</a>



<a href="https://msdn.microsoft.com/2db24a30-0e4e-4647-8975-c9f584c3a9da">OpenClusterNodeEx</a>
 

 


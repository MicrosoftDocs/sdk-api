---
UID: NF:clusapi.EvictClusterNode
title: EvictClusterNode function
author: windows-sdk-content
description: Deletes a node from the cluster database.
old-location: mscs\evictclusternode.htm
tech.root: MsCS
ms.assetid: 0353b640-5fa6-4e83-a7e5-1b4bd2ca16d9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: EvictClusterNode, EvictClusterNode function [Failover Cluster], PCLUSAPI_EVICT_CLUSTER_NODE, PCLUSAPI_EVICT_CLUSTER_NODE function [Failover Cluster], _wolf_evictclusternode, clusapi/EvictClusterNode, clusapi/PCLUSAPI_EVICT_CLUSTER_NODE, mscs.evictclusternode
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
 - EvictClusterNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvictClusterNode function


## -description


Deletes a  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> from the  <a href="https://msdn.microsoft.com/en-us/library/Aa369094(v=VS.85).aspx">cluster database</a>. The <b>PCLUSAPI_EVICT_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the node to delete.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



To reinstate an evicted node, you must first remove the  <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> from the node and then reinstall it. During installation, choose the <b>Join an Existing Cluster</b> option.




## -see-also




<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 


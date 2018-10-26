---
UID: NF:clusapi.PauseClusterNode
title: PauseClusterNode function
author: windows-sdk-content
description: Requests that a node temporarily suspend its cluster activity. The PCLUSAPI_PAUSE_CLUSTER_NODE type defines a pointer to this function.
old-location: mscs\pauseclusternode.htm
tech.root: mscs
ms.assetid: 23b4ff74-f72f-4227-9b69-ff36fa6ed55b
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: PCLUSAPI_PAUSE_CLUSTER_NODE, PCLUSAPI_PAUSE_CLUSTER_NODE function [Failover Cluster], PauseClusterNode, PauseClusterNode function [Failover Cluster], _wolf_pauseclusternode, clusapi/PCLUSAPI_PAUSE_CLUSTER_NODE, clusapi/PauseClusterNode, mscs.pauseclusternode
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
 - PauseClusterNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PauseClusterNode function


## -description


Requests that a  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> temporarily suspend its <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> activity. The <b>PCLUSAPI_PAUSE_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the node to suspend activity.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



When a node temporarily suspends its cluster activity,  <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">groups</a> cannot be moved to the node. Furthermore, groups that would normally fail over to the node cannot do so when it is in the paused state.

Groups that are owned by a paused node remain owned by the node. A paused node's groups and resources can be taken offline, but they cannot be brought online. Because the paused state is persistent, a paused node that is rebooted continues to be paused when it comes back up.

A paused node is said to be in the <b>ClusterNodePaused</b> state (see  <a href="https://msdn.microsoft.com/94c83582-3d99-4a20-ad58-1af4e8190781">GetClusterNodeState</a>). To resume a node's cluster activity, use the  <a href="https://msdn.microsoft.com/01b98d8d-9235-4133-aa3c-f9ad45be8aaf">ResumeClusterNode</a> function.




## -see-also




<a href="https://msdn.microsoft.com/94c83582-3d99-4a20-ad58-1af4e8190781">GetClusterNodeState</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>



<a href="https://msdn.microsoft.com/01b98d8d-9235-4133-aa3c-f9ad45be8aaf">ResumeClusterNode</a>
 

 


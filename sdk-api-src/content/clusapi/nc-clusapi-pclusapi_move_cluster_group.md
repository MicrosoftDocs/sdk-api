---
UID: NC:clusapi.PCLUSAPI_MOVE_CLUSTER_GROUP
title: PCLUSAPI_MOVE_CLUSTER_GROUP
author: windows-driver-content
description: Moves a group and all of its resources from one node to another.
old-location: mscs\moveclustergroup.htm
old-project: MsCS
ms.assetid: 32408600-5118-47fb-890b-9c31faef2299
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: PCLUSAPI_MOVE_CLUSTER_GROUP, PCLUSAPI_MOVE_CLUSTER_GROUP callback, PCLUSAPI_MOVE_CLUSTER_GROUP callback function [Failover Cluster], _wolf_moveclustergroup, clusapi/PCLUSAPI_MOVE_CLUSTER_GROUP, mscs.moveclustergroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_MOVE_CLUSTER_GROUP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_MOVE_CLUSTER_GROUP callback function


## -description


Moves a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> and all of its  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> from one  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to another. The <b>PCLUSAPI_MOVE_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to be moved.


### -param hDestinationNode [in, optional]

Handle to the node where the moved group should be brought back online or <b>NULL</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is one of the possible error codes.




## -remarks



The return value from the  <i>MoveClusterGroup</i> function does not imply anything about the state of the group or any of its resources. The return value only indicates whether the change of ownership was successful. After returning from  <i>MoveClusterGroup</i>, the cluster always attempts to return the group to the state it was before the move.

If you want your application to ensure a particular state for a resource or a group after a move:

<ol>
<li>Check the state prior to the move. The cluster will attempt to restore that state after the move.</li>
<li>Poll for the state after the move and adjust as necessary. Or create a notification port (see  <a href="https://msdn.microsoft.com/6d69cdd8-b29a-40c5-94c6-908b9bea22ef">Receiving Cluster Events</a>) and wait for a <b>CLUSTER_CHANGE_GROUP_STATE</b> event.</li>
</ol>
When <i>hDestinationNode</i> is set to <b>NULL</b>,  <i>MoveClusterGroup</i> attempts to move the group to the best possible node. If there is no node available that can accept the group, the function fails.  <i>MoveClusterGroup</i> also fails if  <i>MoveClusterGroup</i> determines that the group cannot be brought online on the node identified by the <i>hDestinationNode</i> parameter.

Do not call  <i>MoveClusterGroup</i> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and  <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 


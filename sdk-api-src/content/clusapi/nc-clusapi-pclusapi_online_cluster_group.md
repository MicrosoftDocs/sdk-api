---
UID: NC:clusapi.PCLUSAPI_ONLINE_CLUSTER_GROUP
title: PCLUSAPI_ONLINE_CLUSTER_GROUP
author: windows-driver-content
description: Brings a group online.
old-location: mscs\onlineclustergroup.htm
old-project: MsCS
ms.assetid: 33b4f435-f394-41fc-846f-8e9206c76aa1
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: PCLUSAPI_ONLINE_CLUSTER_GROUP, PCLUSAPI_ONLINE_CLUSTER_GROUP callback, PCLUSAPI_ONLINE_CLUSTER_GROUP callback function [Failover Cluster], _wolf_onlineclustergroup, clusapi/PCLUSAPI_ONLINE_CLUSTER_GROUP, mscs.onlineclustergroup
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
-	PCLUSAPI_ONLINE_CLUSTER_GROUP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_ONLINE_CLUSTER_GROUP callback function


## -description


Brings a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> online. The <b>PCLUSAPI_ONLINE_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to be brought online.


### -param hDestinationNode [in, optional]

Handle to the  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> where the group identified by <i>hGroup</i> should be brought online or <b>NULL</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -remarks



If the group cannot be brought online on the node identified by the <i>hDestinationNode</i> parameter, the  <i>OnlineClusterGroup</i> function fails.

If the <i>hDestinationNode</i> parameter is set to <b>NULL</b>,  <i>OnlineClusterGroup</i> brings the group online on the current node.

Do not call  <i>OnlineClusterGroup</i> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and  <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/465e9eac-6286-4955-a11c-a515c64230da">OfflineClusterGroup</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 


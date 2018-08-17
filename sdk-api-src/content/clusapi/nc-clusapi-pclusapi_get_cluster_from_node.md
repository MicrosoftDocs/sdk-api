---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_FROM_NODE
title: PCLUSAPI_GET_CLUSTER_FROM_NODE
author: windows-sdk-content
description: Returns a handle to the cluster associated with a node.
old-location: mscs\getclusterfromnode.htm
old-project: mscs
ms.assetid: 8cc0f881-fbf2-452c-a044-58939f4e01ea
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_FROM_NODE, PCLUSAPI_GET_CLUSTER_FROM_NODE callback, PCLUSAPI_GET_CLUSTER_FROM_NODE callback function [Failover Cluster], _wolf_getclusterfromnode, clusapi/PCLUSAPI_GET_CLUSTER_FROM_NODE, mscs.getclusterfromnode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_GET_CLUSTER_FROM_NODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_FROM_NODE callback function


## -description


Returns a handle to the <a href="https://msdn.microsoft.com/en-us/library/Aa369114(v=VS.85).aspx">cluster</a> associated with a  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_NODE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the node.


## -returns



If the operation succeeds, the function returns a handle to the cluster that owns the node.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For <i>hNode</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>).  <i>GetClusterFromNode</i> returns another instance of the handle from which <i>hNode</i> was obtained.

Be sure to call  <a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a> on the handle returned from  <i>GetClusterFromNode</i> before the handle goes out of scope. Closing this handle does not invalidate <i>hNode</i> or the cluster handle from which <i>hNode</i> was obtained.




## -see-also




<a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a>



<a href="https://msdn.microsoft.com/e2d90b7e-d181-48b6-a891-b885c24a15ea">CloseClusterNode</a>



<a href="https://msdn.microsoft.com/43e1a74f-3320-4b1a-a946-6485d380dda1">GetClusterFromGroup</a>



<a href="https://msdn.microsoft.com/7c6c6883-0d88-4162-a70d-cb6f1153226e">GetClusterFromNetInterface</a>



<a href="https://msdn.microsoft.com/90ac313a-9f60-4591-b0fa-89d99b007280">GetClusterFromNetwork</a>



<a href="https://msdn.microsoft.com/d0ba93cb-94aa-4c68-b87e-518ee1e5c35c">GetClusterFromResource</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 


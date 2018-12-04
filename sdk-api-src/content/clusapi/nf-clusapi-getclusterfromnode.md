---
UID: NF:clusapi.GetClusterFromNode
title: GetClusterFromNode function
author: windows-sdk-content
description: Returns a handle to the cluster associated with a node.
old-location: mscs\getclusterfromnode.htm
tech.root: mscs
ms.assetid: 8cc0f881-fbf2-452c-a044-58939f4e01ea
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetClusterFromNode, GetClusterFromNode function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_NODE, PCLUSAPI_GET_CLUSTER_FROM_NODE function [Failover Cluster], _wolf_getclusterfromnode, clusapi/GetClusterFromNode, clusapi/PCLUSAPI_GET_CLUSTER_FROM_NODE, mscs.getclusterfromnode
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
 - GetClusterFromNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterFromNode function


## -description


Returns a handle to the <a href="c_gly.htm">cluster</a> associated with a  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_NODE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the node.


## -returns



If the operation succeeds, the function returns a handle to the cluster that owns the node.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For <i>hNode</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>).  <b>GetClusterFromNode</b> returns another instance of the handle from which <i>hNode</i> was obtained.

Be sure to call  <a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a> on the handle returned from  <b>GetClusterFromNode</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hNode</i> or the cluster handle from which <i>hNode</i> was obtained.




## -see-also




<a href="https://msdn.microsoft.com/cf055fd6-b1e1-4262-b205-c7d926522450">CloseCluster</a>



<a href="https://msdn.microsoft.com/e2d90b7e-d181-48b6-a891-b885c24a15ea">CloseClusterNode</a>



<a href="https://msdn.microsoft.com/43e1a74f-3320-4b1a-a946-6485d380dda1">GetClusterFromGroup</a>



<a href="https://msdn.microsoft.com/7c6c6883-0d88-4162-a70d-cb6f1153226e">GetClusterFromNetInterface</a>



<a href="https://msdn.microsoft.com/90ac313a-9f60-4591-b0fa-89d99b007280">GetClusterFromNetwork</a>



<a href="https://msdn.microsoft.com/d0ba93cb-94aa-4c68-b87e-518ee1e5c35c">GetClusterFromResource</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 


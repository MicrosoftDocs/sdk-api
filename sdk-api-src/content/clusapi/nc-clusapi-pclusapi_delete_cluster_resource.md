---
UID: NC:clusapi.PCLUSAPI_DELETE_CLUSTER_RESOURCE
title: PCLUSAPI_DELETE_CLUSTER_RESOURCE
author: windows-driver-content
description: Removes an offline resource from a cluster.
old-location: mscs\deleteclusterresource.htm
old-project: MsCS
ms.assetid: d6a8425c-c926-46d8-b13a-c293f8ed30a8
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PCLUSAPI_DELETE_CLUSTER_RESOURCE, PCLUSAPI_DELETE_CLUSTER_RESOURCE callback, PCLUSAPI_DELETE_CLUSTER_RESOURCE callback function [Failover Cluster], _wolf_deleteclusterresource, clusapi/PCLUSAPI_DELETE_CLUSTER_RESOURCE, mscs.deleteclusterresource
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
-	PCLUSAPI_DELETE_CLUSTER_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_DELETE_CLUSTER_RESOURCE callback function


## -description


Removes an offline  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to an offline resource. You must close this handle separately.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of these values.




## -remarks



<i>DeleteClusterResource</i> does not close the resource handle specified by <i>hResource</i>. To avoid memory leaks, be sure to close this handle with  <a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>.

Do not call  <i>DeleteClusterResource</i> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>



<a href="https://msdn.microsoft.com/c9fe8fa8-57d7-4866-8113-694dc44dae22">CreateClusterResource</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 


---
UID: NC:clusapi.PCLUSAPI_OFFLINE_CLUSTER_RESOURCE
title: PCLUSAPI_OFFLINE_CLUSTER_RESOURCE
author: windows-driver-content
description: Takes a resource offline.
old-location: mscs\offlineclusterresource.htm
old-project: MsCS
ms.assetid: 694dbf3d-3355-44d9-8af0-ea2baae832fd
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PCLUSAPI_OFFLINE_CLUSTER_RESOURCE, PCLUSAPI_OFFLINE_CLUSTER_RESOURCE callback, PCLUSAPI_OFFLINE_CLUSTER_RESOURCE callback function [Failover Cluster], _wolf_offlineclusterresource, clusapi/PCLUSAPI_OFFLINE_CLUSTER_RESOURCE, mscs.offlineclusterresource
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
-	PCLUSAPI_OFFLINE_CLUSTER_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_OFFLINE_CLUSTER_RESOURCE callback function


## -description


Takes a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> offline. The <b>PCLUSAPI_OFFLINE_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the resource to be taken offline.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns one of the following 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



When calling <i>OfflineClusterResource</i> to offline a failed resource, it returns <b>ERROR_SUCCESS</b> instead of <b>ERROR_RESOURCE_FAILED</b>, and the resource will transition to the offline state.

Do not call  <i>OfflineClusterResource</i> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>



<a href="https://msdn.microsoft.com/8ea8d741-f6f7-48eb-9678-bbb53f76a9ec">OnlineClusterResource</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 


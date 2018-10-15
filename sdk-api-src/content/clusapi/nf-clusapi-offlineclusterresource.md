---
UID: NF:clusapi.OfflineClusterResource
title: OfflineClusterResource function
author: windows-sdk-content
description: Takes a resource offline.
old-location: mscs\offlineclusterresource.htm
tech.root: mscs
ms.assetid: 694dbf3d-3355-44d9-8af0-ea2baae832fd
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: OfflineClusterResource, OfflineClusterResource function [Failover Cluster], PCLUSAPI_OFFLINE_CLUSTER_RESOURCE, PCLUSAPI_OFFLINE_CLUSTER_RESOURCE function [Failover Cluster], _wolf_offlineclusterresource, clusapi/OfflineClusterResource, clusapi/PCLUSAPI_OFFLINE_CLUSTER_RESOURCE, mscs.offlineclusterresource
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - OfflineClusterResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OfflineClusterResource function


## -description


Takes a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> offline. The <b>PCLUSAPI_OFFLINE_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the resource to be taken offline.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns one of the following 
      <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



When calling <b>OfflineClusterResource</b> to offline a failed resource, it returns <b>ERROR_SUCCESS</b> instead of <b>ERROR_RESOURCE_FAILED</b>, and the resource will transition to the offline state.

Do not call  <b>OfflineClusterResource</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa371767(v=VS.85).aspx">Offline</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371770(v=VS.85).aspx">Online</a>



<a href="https://msdn.microsoft.com/8ea8d741-f6f7-48eb-9678-bbb53f76a9ec">OnlineClusterResource</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 


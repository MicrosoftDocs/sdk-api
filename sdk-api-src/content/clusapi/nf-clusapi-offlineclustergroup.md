---
UID: NF:clusapi.OfflineClusterGroup
title: OfflineClusterGroup function
author: windows-sdk-content
description: Takes a group offline.
old-location: mscs\offlineclustergroup.htm
old-project: mscs
ms.assetid: 465e9eac-6286-4955-a11c-a515c64230da
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OfflineClusterGroup, OfflineClusterGroup function [Failover Cluster], PCLUSAPI_OFFLINE_CLUSTER_GROUP, PCLUSAPI_OFFLINE_CLUSTER_GROUP function [Failover Cluster], _wolf_offlineclustergroup, clusapi/OfflineClusterGroup, clusapi/PCLUSAPI_OFFLINE_CLUSTER_GROUP, mscs.offlineclustergroup
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - OfflineClusterGroup
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# OfflineClusterGroup function


## -description


Takes a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> offline. The <b>PCLUSAPI_OFFLINE_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to be taken offline.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is one of the possible error codes.




## -remarks



Do not call  <b>OfflineClusterGroup</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/33b4f435-f394-41fc-846f-8e9206c76aa1">OnlineClusterGroup</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 


---
UID: NF:clusapi.OfflineClusterGroup
title: OfflineClusterGroup function
author: windows-sdk-content
description: Takes a group offline.
old-location: mscs\offlineclustergroup.htm
tech.root: mscs
ms.assetid: 465e9eac-6286-4955-a11c-a515c64230da
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: OfflineClusterGroup, OfflineClusterGroup function [Failover Cluster], PCLUSAPI_OFFLINE_CLUSTER_GROUP, PCLUSAPI_OFFLINE_CLUSTER_GROUP function [Failover Cluster], _wolf_offlineclustergroup, clusapi/OfflineClusterGroup, clusapi/PCLUSAPI_OFFLINE_CLUSTER_GROUP, mscs.offlineclustergroup
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
 - OfflineClusterGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OfflineClusterGroup function


## -description


Takes a  <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> offline. The <b>PCLUSAPI_OFFLINE_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to be taken offline.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. The following is one of the possible error codes.




## -remarks



Do not call  <b>OfflineClusterGroup</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/33b4f435-f394-41fc-846f-8e9206c76aa1">OnlineClusterGroup</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 


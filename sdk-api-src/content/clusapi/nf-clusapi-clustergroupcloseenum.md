---
UID: NF:clusapi.ClusterGroupCloseEnum
title: ClusterGroupCloseEnum function
author: windows-sdk-content
description: Closes a group enumeration handle.
old-location: mscs\clustergroupcloseenum.htm
tech.root: mscs
ms.assetid: 9bdab6b9-a54d-4166-988c-effdeb2ab254
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterGroupCloseEnum, ClusterGroupCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM, PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM function [Failover Cluster], _wolf_clustergroupcloseenum, clusapi/ClusterGroupCloseEnum, clusapi/PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM, mscs.clustergroupcloseenum
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
 - ClusterGroupCloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterGroupCloseEnum function


## -description


Closes a  <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnum [in]

Enumeration handle to close.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/fffcae88-8df0-487f-9f6d-bc3560283ef1">ClusterGroupEnum</a>



<a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a>
 

 


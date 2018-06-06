---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM
title: PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM
author: windows-sdk-content
description: Closes a group enumeration handle.
old-location: mscs\clustergroupcloseenum.htm
old-project: MsCS
ms.assetid: 9bdab6b9-a54d-4166-988c-effdeb2ab254
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM, PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM callback, PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM callback function [Failover Cluster], _wolf_clustergroupcloseenum, clusapi/PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM, mscs.clustergroupcloseenum
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
 - PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM callback function


## -description


Closes a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_GROUP_CLOSE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnum [in]

Enumeration handle to close.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/fffcae88-8df0-487f-9f6d-bc3560283ef1">ClusterGroupEnum</a>



<a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a>
 

 


---
UID: NC:clusapi.PCLUSAPI_CLUSTER_CLOSE_ENUM
title: PCLUSAPI_CLUSTER_CLOSE_ENUM
author: windows-sdk-content
description: Closes a cluster enumeration handle originally opened by ClusterOpenEnum.
old-location: mscs\clustercloseenum.htm
old-project: mscs
ms.assetid: 3d7e45a0-d580-4d14-8795-2418bba40c73
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_CLUSTER_CLOSE_ENUM, PCLUSAPI_CLUSTER_CLOSE_ENUM callback, PCLUSAPI_CLUSTER_CLOSE_ENUM callback function [Failover Cluster], _wolf_clustercloseenum, clusapi/PCLUSAPI_CLUSTER_CLOSE_ENUM, mscs.clustercloseenum
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
 - PCLUSAPI_CLUSTER_CLOSE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_CLOSE_ENUM callback function


## -description


Closes a cluster enumeration handle originally opened by  <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a>.


## -parameters




### -param hEnum [in]

Cluster enumeration handle to close. This is a handle originally returned by the  <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a> function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7511ac6-04cb-407b-90aa-3382c5160cb6">ClusterEnum</a>



<a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a>
 

 


---
UID: NC:clusapi.PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM
title: PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM
author: windows-sdk-content
description: Closes a resource type enumeration handle.
old-location: mscs\clusterresourcetypecloseenum.htm
old-project: MsCS
ms.assetid: c6524604-7a73-414c-95bb-dce9524f3295
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM callback, PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM callback function [Failover Cluster], _wolf_clusterresourcetypecloseenum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM, mscs.clusterresourcetypecloseenum
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
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM callback function


## -description


Closes a <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hResTypeEnum [in]

Enumeration handle to be closed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21">ClusterResourceTypeEnum</a>



<a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a>
 

 


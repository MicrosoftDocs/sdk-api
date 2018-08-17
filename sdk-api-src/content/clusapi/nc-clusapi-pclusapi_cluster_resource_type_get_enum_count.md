---
UID: NC:clusapi.PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT
title: PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT
author: windows-sdk-content
description: Returns the number of cluster objects associated with a resource_type enumeration handle.
old-location: mscs\clusterresourcetypegetenumcount.htm
old-project: mscs
ms.assetid: 1960dc1a-778e-4bad-b6ad-07c0a8547cc6
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT callback, PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT callback function [Failover Cluster], _wolf_clusterresourcetypegetenumcount, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT, mscs.clusterresourcetypegetenumcount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT callback function


## -description


Returns the number of  <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> associated with a  <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource_type</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hResTypeEnum [in]

Handle to a resource type enumeration. This handle is obtained from  <a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



<i>ClusterResourceTypeGetEnumCount</i> returns the number of objects associated with the enumeration handle.




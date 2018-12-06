---
UID: NF:clusapi.ClusterResourceTypeGetEnumCount
title: ClusterResourceTypeGetEnumCount function
author: windows-sdk-content
description: Returns the number of cluster objects associated with a resource_type enumeration handle.
old-location: mscs\clusterresourcetypegetenumcount.htm
tech.root: mscs
ms.assetid: 1960dc1a-778e-4bad-b6ad-07c0a8547cc6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterResourceTypeGetEnumCount, ClusterResourceTypeGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT function [Failover Cluster], _wolf_clusterresourcetypegetenumcount, clusapi/ClusterResourceTypeGetEnumCount, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT, mscs.clusterresourcetypegetenumcount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - ClusterResourceTypeGetEnumCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceTypeGetEnumCount function


## -description


Returns the number of  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> associated with a  <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource_type</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hResTypeEnum [in]

Handle to a resource type enumeration. This handle is obtained from  <a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



<b>ClusterResourceTypeGetEnumCount</b> returns the number of objects associated with the enumeration handle.




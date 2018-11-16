---
UID: NF:clusapi.ClusterResourceGetEnumCount
title: ClusterResourceGetEnumCount function
author: windows-sdk-content
description: Returns the number of cluster objects associated with a resource enumeration handle.
old-location: mscs\clusterresourcegetenumcount.htm
tech.root: MsCS
ms.assetid: f837d57a-e7eb-4262-a1a3-e3bf9948cf09
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ClusterResourceGetEnumCount, ClusterResourceGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT function [Failover Cluster], _wolf_clusterresourcegetenumcount, clusapi/ClusterResourceGetEnumCount, clusapi/PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT, mscs.clusterresourcegetenumcount
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
 - ClusterResourceGetEnumCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterResourceGetEnumCount
: 
---

# ClusterResourceGetEnumCount function


## -description


Returns the number of  <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> associated with a  <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hResEnum [in]

Handle to a resource enumeration. This handle is obtained from  <a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



<b>ClusterResourceGetEnumCount</b> returns the number of objects associated with the enumeration handle.




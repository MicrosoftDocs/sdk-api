---
UID: NF:clusapi.ClusterResourceGetEnumCount
title: ClusterResourceGetEnumCount function
author: windows-sdk-content
description: Returns the number of cluster objects associated with a resource enumeration handle.
old-location: mscs\clusterresourcegetenumcount.htm
tech.root: mscs
ms.assetid: f837d57a-e7eb-4262-a1a3-e3bf9948cf09
ms.author: windowssdkdev
ms.date: 11/02/2018
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
---

# ClusterResourceGetEnumCount function


## -description


Returns the number of  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> associated with a  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hResEnum [in]

Handle to a resource enumeration. This handle is obtained from  <a href="https://msdn.microsoft.com/f801401f-f49d-41de-b88b-b832330eeccf">ClusterResourceOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



<b>ClusterResourceGetEnumCount</b> returns the number of objects associated with the enumeration handle.




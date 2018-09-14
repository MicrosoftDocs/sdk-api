---
UID: NF:clusapi.ClusterNetworkGetEnumCount
title: ClusterNetworkGetEnumCount function
author: windows-sdk-content
description: Returns the number of cluster objects associated with a network enumeration handle.
old-location: mscs\clusternetworkgetenumcount.htm
tech.root: mscs
ms.assetid: b3397d85-4e9a-4ee8-ba81-25185e2d46fd
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ClusterNetworkGetEnumCount, ClusterNetworkGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT function [Failover Cluster], _wolf_clusternetworkgetenumcount, clusapi/ClusterNetworkGetEnumCount, clusapi/PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT, mscs.clusternetworkgetenumcount
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
api_name:
 - ClusterNetworkGetEnumCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNetworkGetEnumCount function


## -description


Returns the number of <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> associated with a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hNetworkEnum [in]

Handle to a network enumeration. This handle is obtained from 
      <a href="https://msdn.microsoft.com/59f6fd26-1d96-4b04-858d-bfd3e4d25d01">ClusterNetworkOpenEnum</a>. A valid handle is 
      required. This parameter cannot be <b>NULL</b>.


## -returns



<b>ClusterNetworkGetEnumCount</b> returns the 
       number of objects associated with the enumeration handle.




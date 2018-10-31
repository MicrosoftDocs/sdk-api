---
UID: NF:clusapi.ClusterNetworkCloseEnum
title: ClusterNetworkCloseEnum function
author: windows-sdk-content
description: Closes a network enumeration handle.
old-location: mscs\clusternetworkcloseenum.htm
tech.root: mscs
ms.assetid: 725164c5-dc6d-42f4-a703-06336711e72e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ClusterNetworkCloseEnum, ClusterNetworkCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM, PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM function [Failover Cluster], _wolf_clusternetworkcloseenum, clusapi/ClusterNetworkCloseEnum, clusapi/PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM, mscs.clusternetworkcloseenum
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
 - ClusterNetworkCloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNetworkCloseEnum function


## -description


Closes a  <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hNetworkEnum [in]

Handle to the network enumerator to close. This is a handle originally returned by the  <a href="https://msdn.microsoft.com/59f6fd26-1d96-4b04-858d-bfd3e4d25d01">ClusterNetworkOpenEnum</a> function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/41cfb436-7494-4065-b287-075c4c771278">ClusterNetworkEnum</a>



<a href="https://msdn.microsoft.com/59f6fd26-1d96-4b04-858d-bfd3e4d25d01">ClusterNetworkOpenEnum</a>
 

 


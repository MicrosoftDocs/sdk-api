---
UID: NF:clusapi.GetClusterNetworkState
title: GetClusterNetworkState function
author: windows-sdk-content
description: Current state of a network.
old-location: mscs\getclusternetworkstate.htm
tech.root: mscs
ms.assetid: 7fdbc0cf-fa7b-4b48-bd3c-46f174fc514a
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: GetClusterNetworkState, GetClusterNetworkState function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NETWORK_STATE, PCLUSAPI_GET_CLUSTER_NETWORK_STATE function [Failover Cluster], _wolf_getclusternetworkstate, clusapi/GetClusterNetworkState, clusapi/PCLUSAPI_GET_CLUSTER_NETWORK_STATE, mscs.getclusternetworkstate
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
 - GetClusterNetworkState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterNetworkState function


## -description


Returns 
    the current state of a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>. The <b>PCLUSAPI_GET_CLUSTER_NETWORK_STATE</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to the network for which state information should be returned.


## -returns



<b>GetClusterNetworkState</b> returns the current 
       state of the network, which is represented by one of the following values enumerated by the 
       <a href="https://msdn.microsoft.com/1a9e3ff0-eb5a-4a2e-ae19-e70213dc1a4a">CLUSTER_NETWORK_STATE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1a9e3ff0-eb5a-4a2e-ae19-e70213dc1a4a">CLUSTER_NETWORK_STATE</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 


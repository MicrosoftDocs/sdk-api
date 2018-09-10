---
UID: NF:clusapi.GetClusterNetInterfaceState
title: GetClusterNetInterfaceState function
author: windows-sdk-content
description: Returns the current state of a network interface.
old-location: mscs\getclusternetinterfacestate.htm
tech.root: mscs
ms.assetid: d84a5e3f-d0f9-4345-b008-e15c277dcbd5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetClusterNetInterfaceState, GetClusterNetInterfaceState function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE, PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE function [Failover Cluster], _wolf_getclusternetinterfacestate, clusapi/GetClusterNetInterfaceState, clusapi/PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE, mscs.getclusternetinterfacestate
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
 - GetClusterNetInterfaceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterNetInterfaceState function


## -description


Returns the current state of a 
    <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>. The <b>PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE</b> type defines a pointer to this function.


## -parameters




### -param hNetInterface [in]

Handle to the network interface for which state information should be returned.


## -returns



<b>GetClusterNetInterfaceState</b> returns 
       the current state of the network interface, which is represented by one of the following values enumerated by 
       the <a href="https://msdn.microsoft.com/8b4dc26c-0bac-4ff1-b5ae-4524c81ccdf7">CLUSTER_NETINTERFACE_STATE</a> 
       enumeration.




## -see-also




<a href="https://msdn.microsoft.com/8b4dc26c-0bac-4ff1-b5ae-4524c81ccdf7">CLUSTER_NETINTERFACE_STATE</a>



<a href="https://msdn.microsoft.com/1198ad57-ea47-428f-8867-061afbfc7709">OpenClusterNetInterface</a>



<a href="https://msdn.microsoft.com/3bc6bec3-bfe4-4ab4-8ad3-c42eba6d7cba">State Property of the ClusNetInterface Object</a>
 

 


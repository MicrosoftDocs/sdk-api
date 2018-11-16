---
UID: NF:clusapi.ClusterNetworkOpenEnum
title: ClusterNetworkOpenEnum function
author: windows-sdk-content
description: Opens an enumerator for iterating through objects on a network.
old-location: mscs\clusternetworkopenenum.htm
tech.root: MsCS
ms.assetid: 59f6fd26-1d96-4b04-858d-bfd3e4d25d01
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CLUSTER_NETWORK_ENUM_NETINTERFACES, ClusterNetworkOpenEnum, ClusterNetworkOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM, PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM function [Failover Cluster], _wolf_clusternetworkopenenum, clusapi/ClusterNetworkOpenEnum, clusapi/PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM, mscs.clusternetworkopenenum
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
 - ClusterNetworkOpenEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterNetworkOpenEnum
: 
---

# ClusterNetworkOpenEnum function


## -description


Opens an enumerator for iterating through <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">objects</a> on a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a>. The <b>PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

A handle to a network.


### -param dwType [in]

A bitmask that describes the type of objects to be enumerated. One or more of the following values 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309153(v=VS.85).aspx">CLUSTER_NETWORK_ENUM</a> enumeration are valid.



#### CLUSTER_NETWORK_ENUM_NETINTERFACES (1)

Enumerates the network interface objects on the network.


## -returns



If the operation was successful, 
       <b>ClusterNetworkOpenEnum</b> returns a handle to a 
        network enumerator.

If the operation fails, the function returns <b>NULL</b>. For 
        more information about the error, call the function 
        <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Applications call the <b>ClusterNetworkOpenEnum</b> 
     function to create a particular type of enumerator. 
     <b>ClusterNetworkOpenEnum</b> can create enumerators 
     for iterating through all of the objects on a network or only the network interface objects. 
     <b>ClusterNetworkOpenEnum</b> returns a handle that 
     can be passed to <a href="https://msdn.microsoft.com/41cfb436-7494-4065-b287-075c4c771278">ClusterNetworkEnum</a> to access each 
     of the objects to be enumerated and to 
     <a href="https://msdn.microsoft.com/725164c5-dc6d-42f4-a703-06336711e72e">ClusterNetworkCloseEnum</a> to release the 
     enumerator.


#### Examples

See <a href="https://msdn.microsoft.com/en-us/library/Aa369563(v=VS.85).aspx">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa371731(v=VS.85).aspx">Cluster Network Management Functions</a>



<a href="https://msdn.microsoft.com/725164c5-dc6d-42f4-a703-06336711e72e">ClusterNetworkCloseEnum</a>



<a href="https://msdn.microsoft.com/41cfb436-7494-4065-b287-075c4c771278">ClusterNetworkEnum</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 


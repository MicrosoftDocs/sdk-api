---
UID: NF:clusapi.ClusterNetworkEnum
title: ClusterNetworkEnum function
author: windows-sdk-content
description: Enumerates cluster objects on a network, returning the name of one object with each call.
old-location: mscs\clusternetworkenum.htm
tech.root: MsCS
ms.assetid: 41cfb436-7494-4065-b287-075c4c771278
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CLUSTER_NETWORK_ENUM_NETINTERFACES, ClusterNetworkEnum, ClusterNetworkEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NETWORK_ENUM, PCLUSAPI_CLUSTER_NETWORK_ENUM function [Failover Cluster], _wolf_clusternetworkenum, clusapi/ClusterNetworkEnum, clusapi/PCLUSAPI_CLUSTER_NETWORK_ENUM, mscs.clusternetworkenum
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
 - ClusterNetworkEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNetworkEnum function


## -description


Enumerates <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> on a 
    <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>, returning the name of one object with each call. The <b>PCLUSAPI_CLUSTER_NETWORK_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hNetworkEnum [in]

A handle to an existing enumeration object originally returned by the 
       <a href="https://msdn.microsoft.com/59f6fd26-1d96-4b04-858d-bfd3e4d25d01">ClusterNetworkOpenEnum</a> function.


### -param dwIndex [in]

The index used to identify the next entry to be enumerated. This parameter should be zero for the first call 
       to <b>ClusterNetworkEnum</b> and then incremented for 
       subsequent calls.


### -param lpdwType [out]

A pointer to the type of object returned. The following value of the 
       <a href="https://msdn.microsoft.com/f5b02ce2-92d0-4ae7-a5bb-8e5d9c987095">CLUSTER_NETWORK_ENUM</a> enumeration is returned with 
       each call.



#### CLUSTER_NETWORK_ENUM_NETINTERFACES (1)

The object is a <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>.


### -param lpszName [out]

A pointer to a null-terminated Unicode string containing the name of the returned object.


### -param lpcchName [in, out]

A pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


## -returns



The function returns one of the following values.




## -remarks



The <b>ClusterNetworkEnum</b> function is typically 
     used to iterate through a collection of objects of one or more types belonging to a network object. If, for 
     example, an application wants to enumerate all of the 
     <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a> objects on a network, it 
     calls <a href="https://msdn.microsoft.com/59f6fd26-1d96-4b04-858d-bfd3e4d25d01">ClusterNetworkOpenEnum</a> to 
     open a network enumerator that can process network interface objects. The <i>dwType</i> 
     parameter is set to <b>CLUSTER_NETWORK_ENUM_NETINTERFACES</b> to specify network interfaces 
     as the object type to be enumerated. With the handle that 
     <a href="https://msdn.microsoft.com/59f6fd26-1d96-4b04-858d-bfd3e4d25d01">ClusterNetworkOpenEnum</a> returns, 
     the application calls <b>ClusterNetworkEnum</b> 
     repeatedly to retrieve each of the objects. The <i>lpdwType</i> parameter points to the type 
     of object that is retrieved.

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.


#### Examples

See <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f5b02ce2-92d0-4ae7-a5bb-8e5d9c987095">CLUSTER_NETWORK_ENUM</a>



<a href="https://msdn.microsoft.com/7908db54-f432-4aee-aaf4-91f763ffa3a0">Cluster Network Management Functions</a>



<a href="https://msdn.microsoft.com/725164c5-dc6d-42f4-a703-06336711e72e">ClusterNetworkCloseEnum</a>



<a href="https://msdn.microsoft.com/59f6fd26-1d96-4b04-858d-bfd3e4d25d01">ClusterNetworkOpenEnum</a>
 

 


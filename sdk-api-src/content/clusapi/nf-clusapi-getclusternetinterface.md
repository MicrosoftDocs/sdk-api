---
UID: NF:clusapi.GetClusterNetInterface
title: GetClusterNetInterface function
author: windows-sdk-content
description: Returns the name of a node's interface to a network in a cluster.
old-location: mscs\getclusternetinterface.htm
tech.root: mscs
ms.assetid: b9bca010-7401-4a2f-95df-a5d0ef3dbfae
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetClusterNetInterface, GetClusterNetInterface function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NET_INTERFACE, PCLUSAPI_GET_CLUSTER_NET_INTERFACE function [Failover Cluster], _wolf_getclusternetinterface, clusapi/GetClusterNetInterface, clusapi/PCLUSAPI_GET_CLUSTER_NET_INTERFACE, mscs.getclusternetinterface
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
 - GetClusterNetInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterNetInterface function


## -description


Returns the name of a  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node's</a> interface to a  <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a> in a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. The <b>PCLUSAPI_GET_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster.


### -param lpszNodeName [in]

Pointer to a null-terminated Unicode string containing the name of the node in the cluster.


### -param lpszNetworkName [in]

Pointer to a null-terminated Unicode string containing the name of the network.


### -param lpszInterfaceName [out]

Pointer to an output buffer holding the name of the  <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interface</a>.


### -param lpcchInterfaceName [in, out]

Pointer to the size of the <i>lpszInterfaceName</i> buffer as a count of characters. On input, specify the maximum number of characters the buffer can hold, including the terminating <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding the terminating <b>NULL</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. The following is one of the possible values.




## -remarks



Note that <i>lpcchInterfaceName</i> refers to a count of characters and not a count of bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing buffers, see  <a href="https://msdn.microsoft.com/en-us/library/Aa369338(v=VS.85).aspx">Data Size Conventions</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 


---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_NET_INTERFACE
title: PCLUSAPI_GET_CLUSTER_NET_INTERFACE
author: windows-driver-content
description: Returns the name of a node's interface to a network in a cluster.
old-location: mscs\getclusternetinterface.htm
old-project: MsCS
ms.assetid: b9bca010-7401-4a2f-95df-a5d0ef3dbfae
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_NET_INTERFACE, PCLUSAPI_GET_CLUSTER_NET_INTERFACE callback function [Failover Cluster], _wolf_getclusternetinterface, clusapi/PCLUSAPI_GET_CLUSTER_NET_INTERFACE, mscs.getclusternetinterface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_GET_CLUSTER_NET_INTERFACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_NET_INTERFACE callback


## -description


Returns the name of a  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node's</a> interface to a  <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> in a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. The <b>PCLUSAPI_GET_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a cluster.


### -param lpszNodeName [in]

Pointer to a null-terminated Unicode string containing the name of the node in the cluster.


### -param lpszNetworkName [in]

Pointer to a null-terminated Unicode string containing the name of the network.


### -param lpszInterfaceName [out]

Pointer to an output buffer holding the name of the  <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>.


### -param lpcchInterfaceName [in, out]

Pointer to the size of the <i>lpszInterfaceName</i> buffer as a count of characters. On input, specify the maximum number of characters the buffer can hold, including the terminating <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding the terminating <b>NULL</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is one of the possible values.




## -remarks



Note that <i>lpcchInterfaceName</i> refers to a count of characters and not a count of bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing buffers, see  <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 


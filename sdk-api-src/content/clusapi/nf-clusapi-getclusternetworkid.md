---
UID: NF:clusapi.GetClusterNetworkId
title: GetClusterNetworkId function
author: windows-sdk-content
description: Returns the identifier of a network.
old-location: mscs\getclusternetworkid.htm
tech.root: mscs
ms.assetid: 25091883-12fa-41b6-9ac0-70bc22db3f05
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetClusterNetworkId, GetClusterNetworkId function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NETWORK_ID, PCLUSAPI_GET_CLUSTER_NETWORK_ID function [Failover Cluster], _wolf_getclusternetworkid, clusapi/GetClusterNetworkId, clusapi/PCLUSAPI_GET_CLUSTER_NETWORK_ID, mscs.getclusternetworkid
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
 - GetClusterNetworkId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterNetworkId function


## -description


Returns the identifier of a  <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>. The <b>PCLUSAPI_GET_CLUSTER_NETWORK_ID</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to a network.


### -param lpszNetworkId [out]

Pointer to the identifier of the network associated with <i>hNetwork</i>, including the null-terminating character.


### -param lpcchName [in, out]

Pointer to the size of the <i>lpszNetworkID</i> buffer as a count of characters. On input, specify the maximum number of characters the buffer can hold, including the terminating <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding the terminating <b>NULL</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is one of the possible values.




## -remarks



Note that <i>lpcchNetworkID</i> refers to a count of characters and not a count of bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing buffers, see  <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.




## -see-also




<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 


---
UID: NF:clusapi.SetClusterNetworkName
title: SetClusterNetworkName function
author: windows-sdk-content
description: Sets the name for a network.
old-location: mscs\setclusternetworkname.htm
tech.root: mscs
ms.assetid: c1b5dcd0-8974-495c-b85a-1d426719e9f9
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_NETWORK_NAME, PCLUSAPI_SET_CLUSTER_NETWORK_NAME function [Failover Cluster], SetClusterNetworkName, SetClusterNetworkName function [Failover Cluster], _wolf_setclusternetworkname, clusapi/PCLUSAPI_SET_CLUSTER_NETWORK_NAME, clusapi/SetClusterNetworkName, mscs.setclusternetworkname
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
 - SetClusterNetworkName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetClusterNetworkName
: 
---

# SetClusterNetworkName function


## -description


Sets the name for a  <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>. The <b>PCLUSAPI_SET_CLUSTER_NETWORK_NAME</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to a network to name.


### -param lpszName [in]

Pointer to a null-terminated Unicode string containing the new network name.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<b>SetClusterNetworkName</b> changes the  <a href="https://msdn.microsoft.com/f494788e-4581-4a1a-8b10-24b8715f5fce">Name</a> common property of the network identified by <i>hNetwork</i>. This is the only way that  <b>Name</b>, a read-only property, can be changed.




## -see-also




<a href="https://msdn.microsoft.com/f494788e-4581-4a1a-8b10-24b8715f5fce">Name</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 


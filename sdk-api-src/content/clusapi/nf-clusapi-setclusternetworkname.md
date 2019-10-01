---
UID: NF:clusapi.SetClusterNetworkName
title: SetClusterNetworkName function (clusapi.h)
author: windows-sdk-content
description: Sets the name for a network.
old-location: mscs\setclusternetworkname.htm
tech.root: MsCS
ms.assetid: c1b5dcd0-8974-495c-b85a-1d426719e9f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_NETWORK_NAME, PCLUSAPI_SET_CLUSTER_NETWORK_NAME function [Failover Cluster], SetClusterNetworkName, SetClusterNetworkName function [Failover Cluster], _wolf_setclusternetworkname, clusapi/PCLUSAPI_SET_CLUSTER_NETWORK_NAME, clusapi/SetClusterNetworkName, mscs.setclusternetworkname
ms.topic: function
f1_keywords: 
 - "clusapi/SetClusterNetworkName"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetClusterNetworkName function


## -description


Sets the name for a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/networks">network</a>. The <b>PCLUSAPI_SET_CLUSTER_NETWORK_NAME</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to a network to name.


### -param lpszName [in]

Pointer to a null-terminated Unicode string containing the new network name.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -remarks



<b>SetClusterNetworkName</b> changes the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/networks-name">Name</a> common property of the network identified by <i>hNetwork</i>. This is the only way that  <b>Name</b>, a read-only property, can be changed.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/networks-name">Name</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternetwork">OpenClusterNetwork</a>
 

 


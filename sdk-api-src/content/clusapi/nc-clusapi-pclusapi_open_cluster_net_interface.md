---
UID: NC:clusapi.PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE
title: PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE
author: windows-sdk-content
description: Opens a handle to a network interface.
old-location: mscs\openclusternetinterface.htm
old-project: MsCS
ms.assetid: 1198ad57-ea47-428f-8867-061afbfc7709
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE, PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE callback, PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE callback function [Failover Cluster], _wolf_openclusternetinterface, clusapi/PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE, mscs.openclusternetinterface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE callback function


## -description


Opens a handle to a 
    <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>. The <b>PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


### -param lpszInterfaceName [in]

Pointer to a null-terminated Unicode string containing the name of the network interface to open.


## -returns



If the operation was successful, 
       <i>OpenClusterNetInterface</i> returns an open 
       handle to the specified network interface.




## -see-also




<a href="https://msdn.microsoft.com/e5978e81-790a-4ca7-92b7-d19af31f222e">CloseClusterNetInterface</a>



<a href="https://msdn.microsoft.com/63602522-6425-4c3f-b80f-32ee2c3d6469">Network Interface Management Functions</a>



<a href="https://msdn.microsoft.com/207d6888-35ff-44d4-aac0-915815b9730d">OpenClusterNetInterfaceEx</a>
 

 


---
UID: NF:clusapi.OpenClusterNetwork
title: OpenClusterNetwork function
author: windows-sdk-content
description: Opens a connection to a network and returns a handle to it.
old-location: mscs\openclusternetwork.htm
old-project: mscs
ms.assetid: a888ca91-e56f-42bc-81c5-9235c6fd5172
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: OpenClusterNetwork, OpenClusterNetwork function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NETWORK, PCLUSAPI_OPEN_CLUSTER_NETWORK function [Failover Cluster], _wolf_openclusternetwork, clusapi/OpenClusterNetwork, clusapi/PCLUSAPI_OPEN_CLUSTER_NETWORK, mscs.openclusternetwork
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - OpenClusterNetwork
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# OpenClusterNetwork function


## -description


Opens a connection to a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> and returns a handle 
    to it. The <b>PCLUSAPI_OPEN_CLUSTER_NETWORK</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


### -param lpszNetworkName [in]

Pointer to the name of an existing network.


## -returns



If the operation was successful, 
       <b>OpenClusterNetwork</b> returns a network handle.




## -see-also




<a href="https://msdn.microsoft.com/2d112729-1306-45ff-8845-43032a55ca1c">CloseClusterNetwork</a>



<a href="https://msdn.microsoft.com/7908db54-f432-4aee-aaf4-91f763ffa3a0">Failover Cluster Network Management Functions</a>



<a href="https://msdn.microsoft.com/e21dcfd6-adb6-40a7-9518-5b49988e2901">OpenClusterNetworkEx</a>
 

 


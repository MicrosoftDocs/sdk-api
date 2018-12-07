---
UID: NF:clusapi.OpenClusterNetwork
title: OpenClusterNetwork function
author: windows-sdk-content
description: Opens a connection to a network and returns a handle to it.
old-location: mscs\openclusternetwork.htm
tech.root: mscs
ms.assetid: a888ca91-e56f-42bc-81c5-9235c6fd5172
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OpenClusterNetwork, OpenClusterNetwork function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NETWORK, PCLUSAPI_OPEN_CLUSTER_NETWORK function [Failover Cluster], _wolf_openclusternetwork, clusapi/OpenClusterNetwork, clusapi/PCLUSAPI_OPEN_CLUSTER_NETWORK, mscs.openclusternetwork
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
 - OpenClusterNetwork
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenClusterNetwork function


## -description


Opens a connection to a <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a> and returns a handle 
    to it. The <b>PCLUSAPI_OPEN_CLUSTER_NETWORK</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


### -param lpszNetworkName [in]

Pointer to the name of an existing network.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function 
        <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

</td>
</tr>
</table>
 

If the operation was successful, 
       <b>OpenClusterNetwork</b> returns a network handle.




## -see-also




<a href="https://msdn.microsoft.com/2d112729-1306-45ff-8845-43032a55ca1c">CloseClusterNetwork</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371731(v=VS.85).aspx">Failover Cluster Network Management Functions</a>



<a href="https://msdn.microsoft.com/e21dcfd6-adb6-40a7-9518-5b49988e2901">OpenClusterNetworkEx</a>
 

 


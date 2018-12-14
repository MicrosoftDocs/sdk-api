---
UID: NF:clusapi.OpenClusterNetInterface
title: OpenClusterNetInterface function
author: windows-sdk-content
description: Opens a handle to a network interface.
old-location: mscs\openclusternetinterface.htm
tech.root: mscs
ms.assetid: 1198ad57-ea47-428f-8867-061afbfc7709
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OpenClusterNetInterface, OpenClusterNetInterface function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE, PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE function [Failover Cluster], _wolf_openclusternetinterface, clusapi/OpenClusterNetInterface, clusapi/PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE, mscs.openclusternetinterface
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
 - OpenClusterNetInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenClusterNetInterface function


## -description


Opens a handle to a 
    <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>. The <b>PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


### -param lpszInterfaceName [in]

Pointer to a null-terminated Unicode string containing the name of the network interface to open.


## -returns



If the operation was successful, 
       <b>OpenClusterNetInterface</b> returns an open 
       handle to the specified network interface.

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
 




## -see-also




<a href="https://msdn.microsoft.com/e5978e81-790a-4ca7-92b7-d19af31f222e">CloseClusterNetInterface</a>



<a href="https://msdn.microsoft.com/63602522-6425-4c3f-b80f-32ee2c3d6469">Network Interface Management Functions</a>



<a href="https://msdn.microsoft.com/207d6888-35ff-44d4-aac0-915815b9730d">OpenClusterNetInterfaceEx</a>
 

 


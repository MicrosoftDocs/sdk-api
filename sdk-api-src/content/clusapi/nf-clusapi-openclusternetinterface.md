---
UID: NF:clusapi.OpenClusterNetInterface
title: OpenClusterNetInterface function (clusapi.h)
author: windows-sdk-content
description: Opens a handle to a network interface.
old-location: mscs\openclusternetinterface.htm
tech.root: MsCS
ms.assetid: 1198ad57-ea47-428f-8867-061afbfc7709
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OpenClusterNetInterface, OpenClusterNetInterface function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE, PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE function [Failover Cluster], _wolf_openclusternetinterface, clusapi/OpenClusterNetInterface, clusapi/PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE, mscs.openclusternetinterface
ms.topic: function
f1_keywords: 
 - "clusapi/OpenClusterNetInterface"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenClusterNetInterface function


## -description


Opens a handle to a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>. The <b>PCLUSAPI_OPEN_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.


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
        <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-closeclusternetinterface">CloseClusterNetInterface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/network-interface-management-functions">Network Interface Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternetinterfaceex">OpenClusterNetInterfaceEx</a>
 

 


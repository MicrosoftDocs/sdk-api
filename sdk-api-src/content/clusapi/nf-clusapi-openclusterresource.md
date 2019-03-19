---
UID: NF:clusapi.OpenClusterResource
title: OpenClusterResource function (clusapi.h)
author: windows-sdk-content
description: Opens a resource and returns a handle to it.
old-location: mscs\openclusterresource.htm
tech.root: MsCS
ms.assetid: c699cb00-b999-45b8-b9db-570150e1a65e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OpenClusterResource, OpenClusterResource function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_RESOURCE, PCLUSAPI_OPEN_CLUSTER_RESOURCE function [Failover Cluster], _wolf_openclusterresource, clusapi/OpenClusterResource, clusapi/PCLUSAPI_OPEN_CLUSTER_RESOURCE, mscs.openclusterresource
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - OpenClusterResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenClusterResource function


## -description


Opens a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> and returns a handle to 
    it. The <b>PCLUSAPI_OPEN_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


### -param lpszResourceName [in]

Pointer to a null-terminated Unicode string containing the name of the resource to be opened.

Resource names are not case sensitive. A resource name must be unique within the cluster. The name is set 
       when the resource is created and can be changed using the 
       <a href="https://msdn.microsoft.com/8525a0b4-d37e-4ed3-8914-2c427978de6c">SetClusterResourceName</a> function.


## -returns



If the operation was successful, 
       <b>OpenClusterResource</b> returns a handle to the 
       opened resource.

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
The operation was not successful. For information about the error, call the function 
        <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>



<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/bd5a411f-3cf4-4dc5-89fc-0edc59f7b15a">OpenClusterResourceEx</a>
 

 


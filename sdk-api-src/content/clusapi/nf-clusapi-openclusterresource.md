---
UID: NF:clusapi.OpenClusterResource
title: OpenClusterResource function (clusapi.h)
description: Opens a resource and returns a handle to it. (OpenClusterResource)
helpviewer_keywords: ["OpenClusterResource","OpenClusterResource function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER_RESOURCE","PCLUSAPI_OPEN_CLUSTER_RESOURCE function [Failover Cluster]","_wolf_openclusterresource","clusapi/OpenClusterResource","clusapi/PCLUSAPI_OPEN_CLUSTER_RESOURCE","mscs.openclusterresource"]
old-location: mscs\openclusterresource.htm
tech.root: MsCS
ms.assetid: c699cb00-b999-45b8-b9db-570150e1a65e
ms.date: 12/05/2018
ms.keywords: OpenClusterResource, OpenClusterResource function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_RESOURCE, PCLUSAPI_OPEN_CLUSTER_RESOURCE function [Failover Cluster], _wolf_openclusterresource, clusapi/OpenClusterResource, clusapi/PCLUSAPI_OPEN_CLUSTER_RESOURCE, mscs.openclusterresource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenClusterResource
 - clusapi/OpenClusterResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - OpenClusterResource
---

# OpenClusterResource function


## -description

Opens a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> and returns a handle to 
    it. The <b>PCLUSAPI_OPEN_CLUSTER_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

### -param lpszResourceName [in]

Pointer to a null-terminated Unicode string containing the name of the resource to be opened.

Resource names are not case sensitive. A resource name must be unique within the cluster. The name is set 
       when the resource is created and can be changed using the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-setclusterresourcename">SetClusterResourceName</a> function.

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
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>



<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresourceex">OpenClusterResourceEx</a>

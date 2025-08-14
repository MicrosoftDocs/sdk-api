---
UID: NF:clusapi.CloseClusterResource
title: CloseClusterResource function (clusapi.h)
description: Closes a resource handle.
helpviewer_keywords: ["CloseClusterResource","CloseClusterResource function [Failover Cluster]","PCLUSAPI_CLOSE_CLUSTER_RESOURCE","PCLUSAPI_CLOSE_CLUSTER_RESOURCE function [Failover Cluster]","_wolf_closeclusterresource","clusapi/CloseClusterResource","clusapi/PCLUSAPI_CLOSE_CLUSTER_RESOURCE","mscs.closeclusterresource"]
old-location: mscs\closeclusterresource.htm
tech.root: MsCS
ms.assetid: dbefd7f9-3499-45b3-a5c8-d0000632f61c
ms.date: 12/05/2018
ms.keywords: CloseClusterResource, CloseClusterResource function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_RESOURCE, PCLUSAPI_CLOSE_CLUSTER_RESOURCE function [Failover Cluster], _wolf_closeclusterresource, clusapi/CloseClusterResource, clusapi/PCLUSAPI_CLOSE_CLUSTER_RESOURCE, mscs.closeclusterresource
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
 - CloseClusterResource
 - clusapi/CloseClusterResource
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
 - CloseClusterResource
---

# CloseClusterResource function


## -description

Closes a  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the resource to be closed.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For information about the error, call the function  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-createclusterresource">CreateClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>
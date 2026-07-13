---
UID: NF:clusapi.OpenClusterGroup
title: OpenClusterGroup function (clusapi.h)
description: Opens a failover cluster group and returns a handle to it. (OpenClusterGroup)
helpviewer_keywords: ["OpenClusterGroup","OpenClusterGroup function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER_GROUP","PCLUSAPI_OPEN_CLUSTER_GROUP function [Failover Cluster]","_wolf_openclustergroup","clusapi/OpenClusterGroup","clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP","mscs.openclustergroup"]
old-location: mscs\openclustergroup.htm
tech.root: MsCS
ms.assetid: 0c7ef9d9-d32b-448e-9e07-6befb9b3e338
ms.date: 12/05/2018
ms.keywords: OpenClusterGroup, OpenClusterGroup function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_GROUP, PCLUSAPI_OPEN_CLUSTER_GROUP function [Failover Cluster], _wolf_openclustergroup, clusapi/OpenClusterGroup, clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP, mscs.openclustergroup
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
 - OpenClusterGroup
 - clusapi/OpenClusterGroup
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
 - OpenClusterGroup
---

# OpenClusterGroup function


## -description

Opens a failover cluster <a href="/previous-versions/windows/desktop/mscs/groups">group</a> and returns a handle to 
    it.

## -parameters

### -param hCluster [in]

Handle to a cluster that includes the group to open.

### -param lpszGroupName [in]

Name of the group to open.

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
The operation was not successful. For information about the error, call the function 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>
 

If the operation was successful, 
       <b>OpenClusterGroup</b> returns a group handle.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclustergroup">CloseClusterGroup</a>



<a href="/previous-versions/windows/desktop/mscs/group-management-functions">Group Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroupex">OpenClusterGroupEx</a>

---
UID: NF:clusapi.OfflineClusterResource
title: OfflineClusterResource function (clusapi.h)
description: Takes a resource offline.
helpviewer_keywords: ["OfflineClusterResource","OfflineClusterResource function [Failover Cluster]","PCLUSAPI_OFFLINE_CLUSTER_RESOURCE","PCLUSAPI_OFFLINE_CLUSTER_RESOURCE function [Failover Cluster]","_wolf_offlineclusterresource","clusapi/OfflineClusterResource","clusapi/PCLUSAPI_OFFLINE_CLUSTER_RESOURCE","mscs.offlineclusterresource"]
old-location: mscs\offlineclusterresource.htm
tech.root: MsCS
ms.assetid: 694dbf3d-3355-44d9-8af0-ea2baae832fd
ms.date: 12/05/2018
ms.keywords: OfflineClusterResource, OfflineClusterResource function [Failover Cluster], PCLUSAPI_OFFLINE_CLUSTER_RESOURCE, PCLUSAPI_OFFLINE_CLUSTER_RESOURCE function [Failover Cluster], _wolf_offlineclusterresource, clusapi/OfflineClusterResource, clusapi/PCLUSAPI_OFFLINE_CLUSTER_RESOURCE, mscs.offlineclusterresource
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
 - OfflineClusterResource
 - clusapi/OfflineClusterResource
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - OfflineClusterResource
---

# OfflineClusterResource function


## -description

Takes a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> offline. The <b>PCLUSAPI_OFFLINE_CLUSTER_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the resource to be taken offline.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns one of the following 
      <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The resource or one of the resources it depends on has returned <b>ERROR_IO_PENDING</b> from its 
        <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> entry point function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_FAILED</b></dt>
</dl>
</td>
<td width="60%">
This system error code is not returned.

<b>Windows Server 2008 Datacenter and Windows Server 2008 Enterprise:  </b>The function attempted to take offline a failed resource, so the failed resource has not been transitioned to an offline state.

</td>
</tr>
</table>

## -remarks

When calling <b>OfflineClusterResource</b> to offline a failed resource, it returns <b>ERROR_SUCCESS</b> instead of <b>ERROR_RESOURCE_FAILED</b>, and the resource will transition to the offline state.

Do not call  <b>OfflineClusterResource</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-onlineclusterresource">OnlineClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>
---
UID: NF:clusapi.OnlineClusterResource
title: OnlineClusterResource function (clusapi.h)
description: Brings an offline or failed resource online. (OnlineClusterResource)
helpviewer_keywords: ["OnlineClusterResource","OnlineClusterResource function [Failover Cluster]","PCLUSAPI_ONLINE_CLUSTER_RESOURCE","PCLUSAPI_ONLINE_CLUSTER_RESOURCE function [Failover Cluster]","_wolf_onlineclusterresource","clusapi/OnlineClusterResource","clusapi/PCLUSAPI_ONLINE_CLUSTER_RESOURCE","mscs.onlineclusterresource"]
old-location: mscs\onlineclusterresource.htm
tech.root: MsCS
ms.assetid: 8ea8d741-f6f7-48eb-9678-bbb53f76a9ec
ms.date: 12/05/2018
ms.keywords: OnlineClusterResource, OnlineClusterResource function [Failover Cluster], PCLUSAPI_ONLINE_CLUSTER_RESOURCE, PCLUSAPI_ONLINE_CLUSTER_RESOURCE function [Failover Cluster], _wolf_onlineclusterresource, clusapi/OnlineClusterResource, clusapi/PCLUSAPI_ONLINE_CLUSTER_RESOURCE, mscs.onlineclusterresource
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
 - OnlineClusterResource
 - clusapi/OnlineClusterResource
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
 - OnlineClusterResource
---

# OnlineClusterResource function


## -description

Brings an offline or failed  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> online. The <b>PCLUSAPI_ONLINE_CLUSTER_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the resource to be brought online.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error code.

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
The resource or one of the resources it depends on has returned <b>ERROR_IO_PENDING</b> from its  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> entry point function.

</td>
</tr>
</table>

## -remarks

Do not call  <b>OnlineClusterResource</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-offlineclusterresource">OfflineClusterResource</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>

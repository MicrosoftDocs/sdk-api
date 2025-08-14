---
UID: NF:clusapi.DeleteClusterResource
title: DeleteClusterResource function (clusapi.h)
description: Removes an offline resource from a cluster.
helpviewer_keywords: ["DeleteClusterResource","DeleteClusterResource function [Failover Cluster]","PCLUSAPI_DELETE_CLUSTER_RESOURCE","PCLUSAPI_DELETE_CLUSTER_RESOURCE function [Failover Cluster]","_wolf_deleteclusterresource","clusapi/DeleteClusterResource","clusapi/PCLUSAPI_DELETE_CLUSTER_RESOURCE","mscs.deleteclusterresource"]
old-location: mscs\deleteclusterresource.htm
tech.root: MsCS
ms.assetid: d6a8425c-c926-46d8-b13a-c293f8ed30a8
ms.date: 12/05/2018
ms.keywords: DeleteClusterResource, DeleteClusterResource function [Failover Cluster], PCLUSAPI_DELETE_CLUSTER_RESOURCE, PCLUSAPI_DELETE_CLUSTER_RESOURCE function [Failover Cluster], _wolf_deleteclusterresource, clusapi/DeleteClusterResource, clusapi/PCLUSAPI_DELETE_CLUSTER_RESOURCE, mscs.deleteclusterresource
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
 - DeleteClusterResource
 - clusapi/DeleteClusterResource
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
 - DeleteClusterResource
---

# DeleteClusterResource function


## -description

Removes an offline  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> from a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to an offline resource. You must close this handle separately.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_ONLINE</b></dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 R2: The resource identified by <i>hResource</i> is not offline currently.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
Windows Server 2012: The resource identified by <i>hResource</i> is not offline currently.

</td>
</tr>
</table>

## -remarks

<b>DeleteClusterResource</b> does not close the resource handle specified by <i>hResource</i>. To avoid memory leaks, be sure to close this handle with  <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>.

Do not call  <b>DeleteClusterResource</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-createclusterresource">CreateClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>
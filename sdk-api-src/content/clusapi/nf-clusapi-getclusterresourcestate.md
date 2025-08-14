---
UID: NF:clusapi.GetClusterResourceState
title: GetClusterResourceState function (clusapi.h)
description: Returns the current state of a resource.
helpviewer_keywords: ["GetClusterResourceState","GetClusterResourceState function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_RESOURCE_STATE","PCLUSAPI_GET_CLUSTER_RESOURCE_STATE function [Failover Cluster]","_wolf_getclusterresourcestate","clusapi/GetClusterResourceState","clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_STATE","mscs.getclusterresourcestate"]
old-location: mscs\getclusterresourcestate.htm
tech.root: MsCS
ms.assetid: c3897c96-743e-4753-8fef-b8defe4f2b00
ms.date: 12/05/2018
ms.keywords: GetClusterResourceState, GetClusterResourceState function [Failover Cluster], PCLUSAPI_GET_CLUSTER_RESOURCE_STATE, PCLUSAPI_GET_CLUSTER_RESOURCE_STATE function [Failover Cluster], _wolf_getclusterresourcestate, clusapi/GetClusterResourceState, clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_STATE, mscs.getclusterresourcestate
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
 - GetClusterResourceState
 - clusapi/GetClusterResourceState
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
 - GetClusterResourceState
---

# GetClusterResourceState function


## -description

Returns 
    the current state of a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The <b>PCLUSAPI_GET_CLUSTER_RESOURCE_STATE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle specifying the resource for which state information should be returned.

### -param lpszNodeName [out, optional]

Pointer to a buffer that receives the name of the specified resource's current owner node as a 
       <b>NULL</b>-terminated Unicode string. Pass <b>NULL</b> if the node name 
       is not required.

### -param lpcchNodeName [in, out, optional]

Pointer to the size of the <i>lpszNodeName</i> buffer as a count of characters. This 
       pointer cannot be <b>NULL</b> unless <i>lpszNodeName</i> is also 
       <b>NULL</b>. On input, specifies the maximum number of characters the buffer can hold, 
       including the terminating <b>NULL</b>. On output, specifies the number of characters in the 
       resulting name, excluding the terminating <b>NULL</b>.

### -param lpszGroupName [out, optional]

Pointer to a buffer that receives the name of the <a href="/previous-versions/windows/desktop/mscs/groups">group</a> that 
       contains the specified resource. The name is returned as a <b>NULL</b>-terminated Unicode 
       string. Pass <b>NULL</b> if the group name is not required.

### -param lpcchGroupName [in, out, optional]

Pointer to the size of the <i>lpszGroupName</i> buffer as a count of characters. This 
       pointer cannot be <b>NULL</b> unless <i>lpszNodeName</i> is also 
       <b>NULL</b>. On input, specifies the maximum number of characters the buffer can hold, 
       including the terminating <b>NULL</b>. On output, specifies the number of characters in the 
       resulting name, excluding the terminating <b>NULL</b>.

## -returns

<b>GetClusterResourceState</b> returns the 
       current state of the resource enumerated from the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a> enumeration, which can be 
       represented by one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterResourceInitializing</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The resource is performing initialization.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterResourceOnline</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The resource is operational and functioning normally.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterResourceOffline</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The resource is not operational. This value will be returned if the resource reported a state of 
         <b>ClusterResourceOffline</b> (3) or 
         <b>ClusterResourceCannotComeOnlineOnThisNode</b> (127).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterResourceFailed</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The resource has failed. This value will be returned if the resource reported a state of 
         <b>ClusterResourceFailed</b> (4) or 
         <b>ClusterResourceCannotComeOnlineOnAnyNode</b> (126).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterResourcePending</b></dt>
<dt>128</dt>
</dl>
</td>
<td width="60%">
The resource is in the process of coming online or going offline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterResourceOnlinePending</b></dt>
<dt>129</dt>
</dl>
</td>
<td width="60%">
The resource is in the process of coming online.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterResourceOfflinePending</b></dt>
<dt>130</dt>
</dl>
</td>
<td width="60%">
The resource is in the process of going offline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterResourceStateUnknown</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function 
         <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -remarks

Do not call <b>GetClusterResourceState</b> from 
     any resource DLL entry point function. 
     <b>GetClusterResourceState</b> can safely be called 
     from a worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/getting-object-states">Getting Object States</a> for an example.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-offlineclusterresource">OfflineClusterResource</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-onlineclusterresource">OnlineClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>
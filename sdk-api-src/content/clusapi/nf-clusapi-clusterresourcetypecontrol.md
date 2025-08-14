---
UID: NF:clusapi.ClusterResourceTypeControl
title: ClusterResourceTypeControl function (clusapi.h)
description: Initiates an operation affecting a resource type. The operation performed depends on the control code passed to the dwControlCode parameter.
helpviewer_keywords: ["ClusterResourceTypeControl","ClusterResourceTypeControl function [Failover Cluster]","_wolf_clusterresourcetypecontrol","clusapi/ClusterResourceTypeControl","mscs.clusterresourcetypecontrol"]
old-location: mscs\clusterresourcetypecontrol.htm
tech.root: MsCS
ms.assetid: 79f4949d-e5ef-4d2e-ac11-0e30b6c566fd
ms.date: 12/05/2018
ms.keywords: ClusterResourceTypeControl, ClusterResourceTypeControl function [Failover Cluster], _wolf_clusterresourcetypecontrol, clusapi/ClusterResourceTypeControl, mscs.clusterresourcetypecontrol
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
 - ClusterResourceTypeControl
 - clusapi/ClusterResourceTypeControl
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
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceTypeControl
---

# ClusterResourceTypeControl function


## -description

Initiates an operation affecting a <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a>. The 
    operation performed depends on the <a href="/previous-versions/windows/desktop/mscs/control-codes">control code</a> passed to the 
    <i>dwControlCode</i> parameter.

## -parameters

### -param hCluster [in]

Handle to the cluster containing the resource type identified in 
       <i>lpszResourceTypeName</i>.

### -param lpszResourceTypeName [in]

Pointer to a <b>NULL</b>-terminated Unicode string containing the name of the resource 
       type to be affected.

### -param hHostNode [in, optional]

Handle to the node hosting the affected resource type.

### -param dwControlCode [in]

A <a href="/previous-versions/windows/desktop/mscs/resource-type-control-codes">resource type control code</a> specifying 
       the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="/previous-versions/windows/desktop/mscs/control-code-architecture">Control Code Architecture</a> and the following 
       topics:

<ul>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-enum-common-properties">CLUSCTL_RESOURCE_TYPE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-enum-private-properties">CLUSCTL_RESOURCE_TYPE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-characteristics">CLUSCTL_RESOURCE_TYPE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-class-info">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-common-properties">CLUSCTL_RESOURCE_TYPE_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-common-property-fmts">CLUSCTL_RESOURCE_TYPE_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-common-resource-property-fmts">CLUSCTL_RESOURCE_TYPE_GET_COMMON_RESOURCE_PROPERTY_FMTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-crypto-checkpoints">CLUSCTL_RESOURCE_TYPE_GET_CRYPTO_CHECKPOINTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-flags">CLUSCTL_RESOURCE_TYPE_GET_FLAGS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-private-properties">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-private-property-fmts">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-private-resource-property-fmts">CLUSCTL_RESOURCE_TYPE_GET_PRIVATE_RESOURCE_PROPERTY_FMTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-registry-checkpoints">CLUSCTL_RESOURCE_TYPE_GET_REGISTRY_CHECKPOINTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-required-dependencies">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-ro-common-properties">CLUSCTL_RESOURCE_TYPE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-ro-private-properties">CLUSCTL_RESOURCE_TYPE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-query-delete">CLUSCTL_RESOURCE_TYPE_QUERY_DELETE</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-set-common-properties">CLUSCTL_RESOURCE_TYPE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-set-private-properties">CLUSCTL_RESOURCE_TYPE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-storage-get-available-disks">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-storage-get-resourceid">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_RESOURCEID</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-unknown">CLUSCTL_RESOURCE_TYPE_UNKNOWN</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-validate-common-properties">CLUSCTL_RESOURCE_TYPE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-validate-private-properties">CLUSCTL_RESOURCE_TYPE_VALIDATE_PRIVATE_PROPERTIES</a>
</li>
</ul>

### -param lpInBuffer [in, optional]

Pointer to the input buffer with information needed for the operation, or <b>NULL</b> if 
       no information is needed.

### -param nInBufferSize [in]

Number of bytes in the buffer pointed to by <i>lpInBuffer</i>.

### -param lpOutBuffer [out, optional]

Pointer to the output buffer with information resulting from the operation, or 
      <b>NULL</b> if nothing will be returned.

### -param nOutBufferSize [in]

Number of bytes in the output buffer pointed to by <i>lpOutBuffer</i>, or zero if the 
       caller does not know how much data will be returned.

### -param lpBytesReturned [out, optional]

Pointer to the number of bytes in the buffer pointed to by <i>lpOutBuffer</i> that were 
       actually filled in as a result of the operation. The caller can pass <b>NULL</b> for 
       <i>lpBytesReturned</i> if 
       <b>ClusterResourceTypeControl</b> does not need 
       to pass back the number of bytes in the output buffer.

## -returns

The function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful. If the operation required an output buffer, 
         <i>lpBytesReturned</i> (if not <b>NULL</b> on input) points to the 
         actual size of the data returned in the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The output buffer pointed to by <i>lpOutBuffer</i> was not large enough to hold the data 
         resulting from the operation. The <i>lpBytesReturned</i> parameter (if not 
         <b>NULL</b> on input) points to the size required for the output buffer. Only operations 
         requiring an output buffer return <b>ERROR_MORE_DATA</b>. If the 
         <i>lpOutBuffer</i> parameter is <b>NULL</b> and the 
         <i>nOutBufferSize</i> parameter is zero, then <b>ERROR_SUCCESS</b> may 
         be returned, not <b>ERROR_MORE_DATA</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/Debug/system-error-codes">System error code</a></b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. If the operation required an output buffer, the value specified by 
         <i>lpBytesReturned</i> is unreliable.

</td>
</tr>
</table>

## -remarks

When <b>ClusterResourceTypeControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i>, and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="/previous-versions/windows/desktop/mscs/lpc-and-rpc-handles">LPC and RPC Handles</a> and 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

<b>ClusterResourceTypeControl</b> is one of the 
     <a href="/previous-versions/windows/desktop/mscs/control-code-functions">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="/previous-versions/windows/desktop/mscs/using-control-codes">Using Control Codes</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/previous-versions/windows/desktop/mscs/resource-type-control-codes">Resource Type Control Codes</a>
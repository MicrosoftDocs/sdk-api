---
UID: NF:clusapi.ClusterNodeControl
title: ClusterNodeControl function (clusapi.h)
description: Initiates an operation that affects a node. The operation performed depends on the control code passed to the dwControlCode parameter.
helpviewer_keywords: ["ClusterNodeControl","ClusterNodeControl function [Failover Cluster]","_wolf_clusternodecontrol","clusapi/ClusterNodeControl","mscs.clusternodecontrol"]
old-location: mscs\clusternodecontrol.htm
tech.root: MsCS
ms.assetid: f6fc8525-a2d3-4643-9372-548df5e30900
ms.date: 12/05/2018
ms.keywords: ClusterNodeControl, ClusterNodeControl function [Failover Cluster], _wolf_clusternodecontrol, clusapi/ClusterNodeControl, mscs.clusternodecontrol
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
 - ClusterNodeControl
 - clusapi/ClusterNodeControl
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
 - ext-ms-win-cluster-clusapi-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterNodeControl
---

# ClusterNodeControl function


## -description

Initiates an 
    operation that affects a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>. The operation performed depends on the 
    <a href="/previous-versions/windows/desktop/mscs/control-codes">control code</a> passed to the 
    <i>dwControlCode</i> parameter.

## -parameters

### -param hNode [in]

Handle to the node to be affected.

### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node that will perform the operation instead of the node 
       specified in <i>hNode</i>. If <b>NULL</b>, the node that handles the call 
       performs the operation.

### -param dwControlCode [in]

A <a href="/previous-versions/windows/desktop/mscs/node-control-codes">node control code</a> specifying the operation to be 
       performed. For the syntax associated with a control code, refer to  
       <a href="/previous-versions/windows/desktop/mscs/control-code-architecture">Control Code Architecture</a> and the following 
       topics:

<ul>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-enum-common-properties">CLUSCTL_NODE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-enum-private-properties">CLUSCTL_NODE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-characteristics">CLUSCTL_NODE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-common-properties">CLUSCTL_NODE_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-common-property-fmts">CLUSCTL_NODE_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-flags">CLUSCTL_NODE_GET_FLAGS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-id">CLUSCTL_NODE_GET_ID</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-name">CLUSCTL_NODE_GET_NAME</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-private-properties">CLUSCTL_NODE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-private-property-fmts">CLUSCTL_NODE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-ro-common-properties">CLUSCTL_NODE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-get-ro-private-properties">CLUSCTL_NODE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-set-common-properties">CLUSCTL_NODE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-set-private-properties">CLUSCTL_NODE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-unknown">CLUSCTL_NODE_UNKNOWN</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-validate-common-properties">CLUSCTL_NODE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-node-validate-private-properties">CLUSCTL_NODE_VALIDATE_PRIVATE_PROPERTIES</a>
</li>
</ul>

### -param lpInBuffer [in, optional]

Pointer to an input buffer containing information needed for the operation, or <b>NULL</b> 
       if no information is needed.

### -param nInBufferSize [in]

The allocated size (in bytes) of the input buffer.

### -param lpOutBuffer [out, optional]

Pointer to an output buffer to receive the data resulting from the operation, or 
       <b>NULL</b> if no data will be returned.

### -param nOutBufferSize [in]

The allocated size (in bytes) of the output buffer.

### -param lpBytesReturned [out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.

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
         <i>lpBytesReturned</i> (if not <b>NULL</b> on input) is 
         unreliable.

</td>
</tr>
</table>

## -remarks

If <b>ClusterNodeControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i> and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="/previous-versions/windows/desktop/mscs/lpc-and-rpc-handles">LPC and RPC Handles</a> and 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

<b>ClusterNodeControl</b> is one of the 
     <a href="/previous-versions/windows/desktop/mscs/control-code-functions">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="/previous-versions/windows/desktop/mscs/using-control-codes">Using Control Codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/node-control-codes">Node Control Codes</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>
---
UID: NF:clusapi.ClusterGroupSetControl
title: ClusterGroupSetControl function (clusapi.h)
description: Initiates an operation affecting a groupset.
helpviewer_keywords: ["ClusterGroupSetControl","ClusterGroupSetControl function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL","PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL function [Failover Cluster]","clusapi/ClusterGroupSetControl","clusapi/PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL","mscs.clustergroupcollectioncontrol"]
old-location: mscs\clustergroupcollectioncontrol.htm
tech.root: MsCS
ms.assetid: 20f0f70a-b300-41b8-b215-e5a3f24db44b
ms.date: 12/05/2018
ms.keywords: ClusterGroupSetControl, ClusterGroupSetControl function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL, PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL function [Failover Cluster], clusapi/ClusterGroupSetControl, clusapi/PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL, mscs.clustergroupcollectioncontrol
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ClusterGroupSetControl
 - clusapi/ClusterGroupSetControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterGroupSetControl
---

# ClusterGroupSetControl function


## -description

Initiates an operation affecting a groupset.

The 
    operation performed depends on the <a href="/previous-versions/windows/desktop/mscs/control-codes">control code</a> passed to the 
    <i>dwControlCode</i> parameter.

## -parameters

### -param hGroupSet [in]

Handle to the groupset to be affected.

### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node to perform the operation represented by the control 
       code. If <b>NULL</b>, the <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> that owns the 
       groupset performs the operation. Specifying <i>hHostNode</i> is optional.

### -param dwControlCode [in]

A <a href="/previous-versions/windows/desktop/mscs/collection-control-codes-">Collection Control Code</a> specifying 
       the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="/previous-versions/windows/desktop/mscs/control-code-architecture">Control Code Architecture</a> and the following 
       topics.

<ul>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-collection-get-common-properties">CLUSCTL_GROUPSET_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-collection-get-groups">CLUSCTL_GROUPSET_GET_GROUPS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-collection-get-provider-groups">CLUSCTL_GROUPSET_GET_PROVIDER_GROUPS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-collection-get-provider-collections">CLUSCTL_GROUPSET_GET_PROVIDER_COLLECTIONS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-collection-get-ro-common-properties">CLUSCTL_GROUPSET_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-collection-set-common-properties">CLUSCTL_GROUPSET_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-provider-groups">CLUSCTL_GROUP_GET_PROVIDER_GROUPS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-provider-collections">CLUSCTL_GROUP_GET_PROVIDER_COLLECTIONS</a>
</li>
</ul>

### -param lpInBuffer [in, optional]

Pointer to an input buffer containing information needed for the operation, or <b>NULL</b> 
       if no information is needed.

### -param cbInBufferSize [in]

The allocated size (in bytes) of the input buffer.

### -param lpOutBuffer [out, optional]

Pointer to an output buffer to receive the data resulting from the operation, or 
       <b>NULL</b> if no data will be returned.

### -param cbOutBufferSize [in]

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
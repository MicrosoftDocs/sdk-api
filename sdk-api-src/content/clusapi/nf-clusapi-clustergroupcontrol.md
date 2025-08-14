---
UID: NF:clusapi.ClusterGroupControl
title: ClusterGroupControl function (clusapi.h)
description: Initiates an operation that affects a group. The operation performed depends on the control code passed to the dwControlCode parameter.
helpviewer_keywords: ["ClusterGroupControl","ClusterGroupControl function [Failover Cluster]","_wolf_clustergroupcontrol","clusapi/ClusterGroupControl","mscs.clustergroupcontrol"]
old-location: mscs\clustergroupcontrol.htm
tech.root: MsCS
ms.assetid: 72896685-a1db-43d7-a5e3-ba380c0624f2
ms.date: 12/05/2018
ms.keywords: ClusterGroupControl, ClusterGroupControl function [Failover Cluster], _wolf_clustergroupcontrol, clusapi/ClusterGroupControl, mscs.clustergroupcontrol
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
 - ClusterGroupControl
 - clusapi/ClusterGroupControl
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
 - ClusterGroupControl
---

# ClusterGroupControl function


## -description

Initiates an 
    operation that affects a <a href="/previous-versions/windows/desktop/mscs/groups">group</a>. The operation performed depends on 
    the <a href="/previous-versions/windows/desktop/mscs/control-codes">control code</a> passed to the 
    <i>dwControlCode</i> parameter.

## -parameters

### -param hGroup [in]

Handle to the group to be affected.

### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node to perform the operation represented by the control 
       code. If <b>NULL</b>, the <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> that owns the 
       group performs the operation. Specifying <i>hHostNode</i> is optional.

### -param dwControlCode [in]

A <a href="/previous-versions/windows/desktop/mscs/group-control-codes">group control code</a> specifying the operation to 
       be performed. For the syntax associated with a control code, refer to  
       <a href="/previous-versions/windows/desktop/mscs/control-code-architecture">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-enum-common-properties">CLUSCTL_GROUP_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-enum-private-properties">CLUSCTL_GROUP_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-characteristics">CLUSCTL_GROUP_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-common-properties">CLUSCTL_GROUP_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-common-property-fmts">CLUSCTL_GROUP_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-flags">CLUSCTL_GROUP_GET_FLAGS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-id">CLUSCTL_GROUP_GET_ID</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-name">CLUSCTL_GROUP_GET_NAME</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-private-properties">CLUSCTL_GROUP_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-private-property-fmts">CLUSCTL_GROUP_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-ro-common-properties">CLUSCTL_GROUP_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-get-ro-private-properties">CLUSCTL_GROUP_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-query-delete">CLUSCTL_GROUP_QUERY_DELETE</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-set-common-properties">CLUSCTL_GROUP_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-set-private-properties">CLUSCTL_GROUP_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-unknown">CLUSCTL_GROUP_UNKNOWN</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-validate-common-properties">CLUSCTL_GROUP_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/mscs/clusctl-group-validate-private-properties">CLUSCTL_GROUP_VALIDATE_PRIVATE_PROPERTIES</a>
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

If <b>ClusterGroupControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i> and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="/previous-versions/windows/desktop/mscs/lpc-and-rpc-handles">LPC and RPC Handles</a> and 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

<b>ClusterGroupControl</b> is one of the 
     <a href="/previous-versions/windows/desktop/mscs/control-code-functions">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="/previous-versions/windows/desktop/mscs/using-control-codes">Using Control Codes</a>.


#### Examples

The following code fragment demonstrates a call to 
      <b>ClusterGroupControl</b>.


``` syntax
// Allocate buffer.
lpPropList = LocalAlloc( LPTR, cbAllocated );

// Initial call.
dwResult = ClusterGroupControl( hCluster,
                                NULL,
                                CLUSCTL_GROUP_GET_COMMON_PROPERTIES, 
                                NULL,
                                0,
                                lpPropList,
                                cbAllocated,
                                &cbReturned );

// If the buffer was too small, reallocate it to the necessary size,
// returned in cbReturned.
if ( dwResult == ERROR_MORE_DATA )
{
  LocalFree( lpPropList );
  cbAllocated = cbReturned;
  lpPropList = LocalAlloc( LPTR, cbAllocated );
  if ( lpPropList == NULL )
  {
    // Respond to error.
  }
  dwResult = ClusterGroupControl( hCluster,
                                  NULL,
                                  CLUSCTL_GROUP_GET_COMMON_PROPERTIES,
                                  NULL,
                                  0,
                                  lpPropList,
                                  cbAllocated,
                                  &cbReturned );
}

if ( dwResult != ERROR_SUCCESS )
{
  // Respond to error.
}
```


## -see-also

<a href="/previous-versions/windows/desktop/mscs/group-control-codes">Group Control Codes</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>

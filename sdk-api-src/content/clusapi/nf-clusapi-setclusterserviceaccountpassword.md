---
UID: NF:clusapi.SetClusterServiceAccountPassword
title: SetClusterServiceAccountPassword function (clusapi.h)
description: Changes the password for the Cluster service user account on all available cluster nodes.
helpviewer_keywords: ["CLUSTER_SET_PASSWORD_IGNORE_DOWN_NODES","PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD","PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD function [Failover Cluster]","SetClusterServiceAccountPassword","SetClusterServiceAccountPassword function [Failover Cluster]","_wolf_setclusterserviceaccountpassword","clusapi/PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD","clusapi/SetClusterServiceAccountPassword","mscs.setclusterserviceaccountpassword"]
old-location: mscs\setclusterserviceaccountpassword.htm
tech.root: MsCS
ms.assetid: 4afadb62-2bea-46ef-b0d6-e327ac96d16f
ms.date: 12/05/2018
ms.keywords: CLUSTER_SET_PASSWORD_IGNORE_DOWN_NODES, PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD, PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD function [Failover Cluster], SetClusterServiceAccountPassword, SetClusterServiceAccountPassword function [Failover Cluster], _wolf_setclusterserviceaccountpassword, clusapi/PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD, clusapi/SetClusterServiceAccountPassword, mscs.setclusterserviceaccountpassword
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Datacenter, Windows Server 2003 Enterprise
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
 - SetClusterServiceAccountPassword
 - clusapi/SetClusterServiceAccountPassword
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
 - SetClusterServiceAccountPassword
---

# SetClusterServiceAccountPassword function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems specified in the 
    Requirements section. Support for this function was removed in Windows Server 2008 and this function does 
    nothing and returns <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Changes the password for the Cluster service user account on all available cluster 
    nodes. The <b>PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD</b> type defines a pointer to this function.

## -parameters

### -param lpszClusterName [in]

<b>NULL</b>-terminated Unicode string specifying the name of the cluster.

### -param lpszNewPassword [in]

<b>NULL</b>-terminated Unicode string specifying the new password for the Cluster service 
       user account.

### -param dwFlags [in, optional]

Optional bitfield of values enumerated from the 
       <a href="/previous-versions/windows/desktop/legacy/cc512182(v=vs.85)">CLUSTER_SET_PASSWORD_FLAGS</a> enumeration 
       containing flags that describe how the password update is to be applied to the cluster.

By default (<i>dwFlags</i> = 0), the function will not proceed unless all cluster nodes 
       are available.



#### CLUSTER_SET_PASSWORD_IGNORE_DOWN_NODES (1 (0x1))

Causes the 
         <b>SetClusterServiceAccountPassword</b> 
         function to proceed even if all nodes are not available. The function will attempt to change the password on 
         as many nodes as it can, but any nodes not in the <b>ClusterNodeUp</b> or 
         <b>ClusterNodePaused</b> states (see 
         <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodestate">GetClusterNodeState</a>) will not be updated.

### -param lpReturnStatusBuffer [out]

Pointer to an output buffer that receives an array of 
       <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-cluster_set_password_status">CLUSTER_SET_PASSWORD_STATUS</a> structures 
       describing the result of the password update for each cluster node. If this parameter is not 
       <b>NULL</b> and the buffer is not large enough to hold the resulting data, the function 
       returns <b>ERROR_MORE_DATA</b> and sets <i>lpcbReturnStatusBufferSize</i> 
       to the required size for the output buffer. If this parameter is <b>NULL</b>, no password 
       update will be performed; the function will set <i>lpcbReturnStatusBufferSize</i> to the 
       required buffer size and return <b>ERROR_SUCCESS</b>.

### -param lpcbReturnStatusBufferSize [in, out]

On input, pointer to a value specifying the size (in bytes) of the output buffer. On output, pointer to a 
       value specifying the actual size (in bytes) of the resulting data. The output size is always specified, even if 
       <i>lpReturnStatusBuffer</i> is <b>NULL</b>. This parameter cannot be 
       <b>NULL</b>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
      <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error 
      codes.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALL_NODES_NOT_AVAILABLE</b></dt>
<dt>5037 (0x13AD)</dt>
</dl>
</td>
<td width="60%">
Some nodes in the cluster are unavailable (that is, not in the 
         <b>ClusterNodeStateUp</b> or <b>ClusterNodeStatePaused</b> states) 
         and the <b>CLUSTER_SET_PASSWORD_IGNORE_DOWN_NODES</b> flag is not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
The output buffer pointed to by <i>lpReturnStatusBuffer</i> was not large enough to hold 
         the resulting data.

</td>
</tr>
</table>

## -remarks

By default, the 
     <b>SetClusterServiceAccountPassword</b> 
     function does nothing unless all nodes in the cluster are available (that is, in the 
     <b>ClusterNodeStateUp</b> or <b>ClusterNodeStatePaused</b> states). You 
     can use the <b>CLUSTER_SET_PASSWORD_IGNORE_DOWN_NODES</b> flag to override this behavior, 
     but note that any node that fails to update the password will be unable to join the cluster until the password is 
     manually updated on that node.

If the new password is the same as the old password on a node, the password update is not applied to that node 
     and <b>ERROR_SUCCESS</b> is returned.

This function does not update the password stored by the domain controllers for the Cluster service user 
     account.

Do not call 
     <b>SetClusterServiceAccountPassword</b> 
     from a resource DLL.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/cc512182(v=vs.85)">CLUSTER_SET_PASSWORD_FLAGS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-cluster_set_password_status">CLUSTER_SET_PASSWORD_STATUS</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Cluster Management Functions</a>
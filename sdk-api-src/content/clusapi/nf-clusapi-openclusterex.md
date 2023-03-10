---
UID: NF:clusapi.OpenClusterEx
title: OpenClusterEx function (clusapi.h)
description: Opens a connection to a cluster and returns a handle to it. (OpenClusterEx)
helpviewer_keywords: ["OpenClusterEx","OpenClusterEx function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER_EX","PCLUSAPI_OPEN_CLUSTER_EX function [Failover Cluster]","clusapi/OpenClusterEx","clusapi/PCLUSAPI_OPEN_CLUSTER_EX","mscs.openclusterex"]
old-location: mscs\openclusterex.htm
tech.root: MsCS
ms.assetid: 688702b7-7525-48d6-9e44-d7c4969565f8
ms.date: 12/05/2018
ms.keywords: OpenClusterEx, OpenClusterEx function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_EX, PCLUSAPI_OPEN_CLUSTER_EX function [Failover Cluster], clusapi/OpenClusterEx, clusapi/PCLUSAPI_OPEN_CLUSTER_EX, mscs.openclusterex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
 - OpenClusterEx
 - clusapi/OpenClusterEx
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
 - OpenClusterEx
---

# OpenClusterEx function


## -description

Opens a connection to a 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to it.

## -parameters

### -param lpszClusterName [in, optional]

Specifies one of the following values:

<ul>
<li>Pointer to a null-terminated Unicode string containing the name of the cluster or one of the cluster 
        <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> expressed as a NetBIOS name, a fully qualified DNS name, or 
        an IP address. This produces an RPC cluster handle.</li>
<li><b>NULL</b>, which produces an LPC handle to the cluster to which the local computer 
        belongs.</li>
</ul>

### -param DesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

### -param GrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.

## -returns

If the operation was successful, <b>OpenClusterEx</b> returns 
       a cluster handle.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. If the target server does not 
        support the <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterex">OpenClusterEx</a> function (for example if 
        the target server is running Windows Server 2008 or earlier) then the 
        <b>GetLastError</b> function will return 
        <b>RPC_S_PROCNUM_OUT_OF_RANGE</b> (1745).

</td>
</tr>
</table>

## -remarks

A cluster handle is a pointer to an internally defined structure which stores information about the RPC or LPC 
     connection to the cluster. Any object handles obtained from the cluster handle will be associated with the RPC or 
     LPC session data stored in the cluster structure. Combining RPC and LPC handles or using handles obtained from 
     different contexts can cause exceptions or other unpredictable results. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/lpc-and-rpc-handles">LPC and RPC Handles</a>.

When finished with a cluster handle, it is important to call 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a> to ensure that all memory is freed and the 
     connection is shut down cleanly.

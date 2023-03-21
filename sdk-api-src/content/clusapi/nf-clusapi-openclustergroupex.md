---
UID: NF:clusapi.OpenClusterGroupEx
title: OpenClusterGroupEx function (clusapi.h)
description: Opens a failover cluster group and returns a handle to it. (OpenClusterGroupEx)
helpviewer_keywords: ["OpenClusterGroupEx","OpenClusterGroupEx function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER_GROUP_EX","PCLUSAPI_OPEN_CLUSTER_GROUP_EX function [Failover Cluster]","clusapi/OpenClusterGroupEx","clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP_EX","mscs.openclustergroupex"]
old-location: mscs\openclustergroupex.htm
tech.root: MsCS
ms.assetid: 240defbb-b9e9-4455-b863-c9b2192f12b7
ms.date: 12/05/2018
ms.keywords: OpenClusterGroupEx, OpenClusterGroupEx function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_GROUP_EX, PCLUSAPI_OPEN_CLUSTER_GROUP_EX function [Failover Cluster], clusapi/OpenClusterGroupEx, clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP_EX, mscs.openclustergroupex
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
 - OpenClusterGroupEx
 - clusapi/OpenClusterGroupEx
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
 - OpenClusterGroupEx
---

# OpenClusterGroupEx function


## -description

Opens a failover cluster <a href="/previous-versions/windows/desktop/mscs/groups">group</a> and returns a handle to 
    it.

## -parameters

### -param hCluster [in]

Handle to a cluster that includes the group to open.

### -param lpszGroupName [in, optional]

Name of the group to open.

### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>.

### -param lpdwGrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.

## -returns

If the operation was successful, 
      <b>OpenClusterGroupEx</b> returns a group handle.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. If the target server does not 
        support the <a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroupex">OpenClusterGroupEx</a> function (for 
        example if the target server is running Windows Server 2008 or earlier) then the 
        <b>GetLastError</b> function will return 
        <b>RPC_S_PROCNUM_OUT_OF_RANGE</b> (1745).

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclustergroup">CloseClusterGroup</a>



<a href="/previous-versions/windows/desktop/mscs/group-management-functions">Group Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>

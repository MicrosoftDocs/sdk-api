---
UID: NF:clusapi.OpenClusterNetInterfaceEx
title: OpenClusterNetInterfaceEx function (clusapi.h)
description: Opens a handle to a network interface. (OpenClusterNetInterfaceEx)
helpviewer_keywords: ["OpenClusterNetInterfaceEx","OpenClusterNetInterfaceEx function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX","PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX function [Failover Cluster]","clusapi/OpenClusterNetInterfaceEx","clusapi/PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX","mscs.openclusternetinterfaceex"]
old-location: mscs\openclusternetinterfaceex.htm
tech.root: MsCS
ms.assetid: 207d6888-35ff-44d4-aac0-915815b9730d
ms.date: 12/05/2018
ms.keywords: OpenClusterNetInterfaceEx, OpenClusterNetInterfaceEx function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX, PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX function [Failover Cluster], clusapi/OpenClusterNetInterfaceEx, clusapi/PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX, mscs.openclusternetinterfaceex
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
 - OpenClusterNetInterfaceEx
 - clusapi/OpenClusterNetInterfaceEx
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
 - OpenClusterNetInterfaceEx
---

# OpenClusterNetInterfaceEx function


## -description

Opens a handle to a 
    <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>.

## -parameters

### -param hCluster [in]

Handle to a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

### -param lpszInterfaceName [in, optional]

Pointer to a null-terminated Unicode string containing the name of the network interface to open.

### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetinterface">OpenClusterNetInterface</a>.

### -param lpdwGrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.

## -returns

If the operation was successful, 
       <b>OpenClusterNetInterfaceEx</b> returns an open 
       handle to the specified network interface.

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
        support the <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetinterfaceex">OpenClusterNetInterfaceEx</a> 
        function (for example if the target server is running Windows Server 2008 or earlier) then the 
        <b>GetLastError</b> function will return 
        <b>RPC_S_PROCNUM_OUT_OF_RANGE</b> (1745).

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternetinterface">CloseClusterNetInterface</a>



<a href="/previous-versions/windows/desktop/mscs/network-interface-management-functions">Network Interface Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetinterface">OpenClusterNetInterface</a>

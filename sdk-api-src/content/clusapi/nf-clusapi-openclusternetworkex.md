---
UID: NF:clusapi.OpenClusterNetworkEx
title: OpenClusterNetworkEx function (clusapi.h)
author: windows-sdk-content
description: Opens a connection to a network and returns a handle to it.
old-location: mscs\openclusternetworkex.htm
tech.root: MsCS
ms.assetid: e21dcfd6-adb6-40a7-9518-5b49988e2901
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OpenClusterNetworkEx, OpenClusterNetworkEx function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NETWORK_EX, PCLUSAPI_OPEN_CLUSTER_NETWORK_EX function [Failover Cluster], clusapi/OpenClusterNetworkEx, clusapi/PCLUSAPI_OPEN_CLUSTER_NETWORK_EX, mscs.openclusternetworkex
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - OpenClusterNetworkEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenClusterNetworkEx function


## -description


Opens a connection to a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> and returns a handle 
    to it.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


### -param lpszNetworkName [in, optional]

Pointer to the name of an existing network.


### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>.


### -param lpdwGrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.


## -returns



If the operation was successful, 
      <b>OpenClusterNetworkEx</b> returns a network 
      handle.

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
        <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. If the target server does not 
        support the <a href="https://msdn.microsoft.com/e21dcfd6-adb6-40a7-9518-5b49988e2901">OpenClusterNetworkEx</a> function 
        (for example if the target server is running Windows Server 2008 or earlier) then the 
        <b>GetLastError</b> function will return 
        <b>RPC_S_PROCNUM_OUT_OF_RANGE</b> (1745).

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2d112729-1306-45ff-8845-43032a55ca1c">CloseClusterNetwork</a>



<a href="https://msdn.microsoft.com/7908db54-f432-4aee-aaf4-91f763ffa3a0">Failover Cluster Network Management Functions</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 


---
UID: NF:clusapi.OpenClusterNetworkEx
title: OpenClusterNetworkEx function
author: windows-sdk-content
description: Opens a connection to a network and returns a handle to it.
old-location: mscs\openclusternetworkex.htm
tech.root: mscs
ms.assetid: e21dcfd6-adb6-40a7-9518-5b49988e2901
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: OpenClusterNetworkEx, OpenClusterNetworkEx function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NETWORK_EX, PCLUSAPI_OPEN_CLUSTER_NETWORK_EX function [Failover Cluster], clusapi/OpenClusterNetworkEx, clusapi/PCLUSAPI_OPEN_CLUSTER_NETWORK_EX, mscs.openclusternetworkex
ms.prod: windows-hardware
ms.technology: windows-devices
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

Handle to a <a href="c_gly.htm">cluster</a>.


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




## -see-also




<a href="https://msdn.microsoft.com/2d112729-1306-45ff-8845-43032a55ca1c">CloseClusterNetwork</a>



<a href="https://msdn.microsoft.com/7908db54-f432-4aee-aaf4-91f763ffa3a0">Failover Cluster Network Management Functions</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 


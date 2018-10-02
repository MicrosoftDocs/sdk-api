---
UID: NF:clusapi.OpenClusterNetInterfaceEx
title: OpenClusterNetInterfaceEx function
author: windows-sdk-content
description: Opens a handle to a network interface.
old-location: mscs\openclusternetinterfaceex.htm
tech.root: MsCS
ms.assetid: 207d6888-35ff-44d4-aac0-915815b9730d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OpenClusterNetInterfaceEx, OpenClusterNetInterfaceEx function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX, PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX function [Failover Cluster], clusapi/OpenClusterNetInterfaceEx, clusapi/PCLUSAPI_OPEN_CLUSTER_NETINTERFACE_EX, mscs.openclusternetinterfaceex
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
 - OpenClusterNetInterfaceEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenClusterNetInterfaceEx function


## -description


Opens a handle to a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interface</a>.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


### -param lpszInterfaceName [in, optional]

Pointer to a null-terminated Unicode string containing the name of the network interface to open.


### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="https://msdn.microsoft.com/1198ad57-ea47-428f-8867-061afbfc7709">OpenClusterNetInterface</a>.


### -param lpdwGrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.


## -returns



If the operation was successful, 
       <b>OpenClusterNetInterfaceEx</b> returns an open 
       handle to the specified network interface.




## -see-also




<a href="https://msdn.microsoft.com/e5978e81-790a-4ca7-92b7-d19af31f222e">CloseClusterNetInterface</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371724(v=VS.85).aspx">Network Interface Management Functions</a>



<a href="https://msdn.microsoft.com/1198ad57-ea47-428f-8867-061afbfc7709">OpenClusterNetInterface</a>
 

 


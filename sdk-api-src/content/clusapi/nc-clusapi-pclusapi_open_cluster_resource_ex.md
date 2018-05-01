---
UID: NC:clusapi.PCLUSAPI_OPEN_CLUSTER_RESOURCE_EX
title: PCLUSAPI_OPEN_CLUSTER_RESOURCE_EX
author: windows-driver-content
description: Opens a resource and returns a handle to it.
old-location: mscs\openclusterresourceex.htm
old-project: MsCS
ms.assetid: bd5a411f-3cf4-4dc5-89fc-0edc59f7b15a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_OPEN_CLUSTER_RESOURCE_EX, PCLUSAPI_OPEN_CLUSTER_RESOURCE_EX callback function [Failover Cluster], clusapi/PCLUSAPI_OPEN_CLUSTER_RESOURCE_EX, mscs.openclusterresourceex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_OPEN_CLUSTER_RESOURCE_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_OPEN_CLUSTER_RESOURCE_EX callback


## -description


Opens a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> and returns a handle to 
    it.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


### -param lpszResourceName [in, optional]

Pointer to a null-terminated Unicode string containing the name of the resource to be opened.

Resource names are not case sensitive. A resource name must be unique within the cluster. The name is set 
       when the resource is created and can be changed using the 
       <a href="https://msdn.microsoft.com/8525a0b4-d37e-4ed3-8914-2c427978de6c">SetClusterResourceName</a> function.


### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>.


### -param lpdwGrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.


## -returns



If the operation was successful, 
      <i>OpenClusterResourceEx</i> returns a handle to the 
      opened resource.




## -see-also




<a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>



<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 


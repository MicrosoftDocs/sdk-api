---
UID: NC:clusapi.PCLUSAPI_OPEN_CLUSTER_NODE_EX
title: PCLUSAPI_OPEN_CLUSTER_NODE_EX
author: windows-sdk-content
description: Opens a node and returns a handle to it.
old-location: mscs\openclusternodeex.htm
old-project: MsCS
ms.assetid: 2db24a30-0e4e-4647-8975-c9f584c3a9da
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_OPEN_CLUSTER_NODE_EX, PCLUSAPI_OPEN_CLUSTER_NODE_EX callback, PCLUSAPI_OPEN_CLUSTER_NODE_EX callback function [Failover Cluster], clusapi/PCLUSAPI_OPEN_CLUSTER_NODE_EX, mscs.openclusternodeex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_OPEN_CLUSTER_NODE_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_OPEN_CLUSTER_NODE_EX callback function


## -description


Opens a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> and returns a handle to it.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> returned from the 
      <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a> or 
      <a href="https://msdn.microsoft.com/688702b7-7525-48d6-9e44-d7c4969565f8">OpenClusterEx</a> functions.


### -param lpszNodeName [in, optional]

Pointer to the NetBIOS name of an existing node. If the DNS name of the node is used, the 
      <i>OpenClusterNodeEx</i> function will fail and 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return 
      <b>ERROR_CLUSTER_NODE_NOT_FOUND</b>.


### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>.


### -param lpdwGrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.


## -returns



If the operation was successful, 
      <i>OpenClusterNodeEx</i> returns a node handle.




## -see-also




<a href="https://msdn.microsoft.com/e2d90b7e-d181-48b6-a891-b885c24a15ea">CloseClusterNode</a>



<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/688702b7-7525-48d6-9e44-d7c4969565f8">OpenClusterEx</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 


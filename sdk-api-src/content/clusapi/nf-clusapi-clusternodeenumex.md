---
UID: NF:clusapi.ClusterNodeEnumEx
title: ClusterNodeEnumEx function
author: windows-sdk-content
description: Retrieves the specified cluster node from a CLUSTER_ENUM_ITEM enumeration.
old-location: mscs\clusternodeenumex.htm
old-project: mscs
ms.assetid: 1F3DFD5C-978B-4943-B4D8-81A7F9D7A3AF
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusterNodeEnumEx, ClusterNodeEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_ENUM_EX, PCLUSAPI_CLUSTER_NODE_ENUM_EX function [Failover Cluster], clusapi/ClusterNodeEnumEx, clusapi/PCLUSAPI_CLUSTER_NODE_ENUM_EX, mscs.clusternodeenumex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.redist: 
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterNodeEnumEx
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterNodeEnumEx function


## -description


Retrieves the specified cluster node from a <a href="https://msdn.microsoft.com/en-us/library/Dn622910(v=VS.85).aspx">CLUSTER_ENUM_ITEM</a> enumeration.


## -parameters




### -param hNodeEnum [in]

A handle to the <a href="https://msdn.microsoft.com/en-us/library/Dn622910(v=VS.85).aspx">CLUSTER_ENUM_ITEM</a> enumeration that contains the cluster node to retrieve.


### -param dwIndex [in]

The index that identifies the next object to enumerate. This parameter should be zero for the first call to the  <a href="https://msdn.microsoft.com/F50FB801-8ACA-40BD-9E89-7E3AF2CA2DA5">ClusterEnumEx</a>  function and then be incremented for subsequent calls.


### -param pItem [in, out]

A pointer that receives the returned cluster node.


### -param cbItem [in, out]

On input, the size of the  <i>pItem</i>    parameter.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes written into the buffer.


## -returns



This function returns DWORD __stdcall.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn622910(v=VS.85).aspx">CLUSTER_ENUM_ITEM</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371760(v=VS.85).aspx">Node Management Functions</a>
 

 


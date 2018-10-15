---
UID: NF:clusapi.ClusterEnumEx
title: ClusterEnumEx function
author: windows-sdk-content
description: Enumerates the objects in a cluster, and then gets the name and properties of the cluster object.
old-location: mscs\clusterenumex.htm
tech.root: mscs
ms.assetid: F50FB801-8ACA-40BD-9E89-7E3AF2CA2DA5
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ClusterEnumEx, ClusterEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_ENUM_EX, PCLUSAPI_CLUSTER_ENUM_EX function [Failover Cluster], clusapi/ClusterEnumEx, clusapi/PCLUSAPI_CLUSTER_ENUM_EX, mscs.clusterenumex
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
 - ClusterEnumEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterEnumEx function


## -description


Enumerates the objects in a cluster, and then gets the name and properties of the cluster object.


## -parameters




### -param hClusterEnum [in]

A handle to the enumerator that is returned by the <a href="https://msdn.microsoft.com/DA35A67E-6F20-47CC-A96A-591702A79EF5">ClusterOpenEnumEx</a> function.


### -param dwIndex [in]

The index that identifies the next cluster object to enumerate. This parameter should be zero for the first call to the  <b>ClusterEnumEx</b>  function and then be  incremented for subsequent calls.


### -param pItem [in, out]

A pointer that receives the returned cluster object properties.


### -param cbItem [in, out]

On input, the size of the  <i>pItem</i>   parameter.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes that are  written into the buffer.


## -returns



This function returns DWORD.




## -see-also




<a href="https://msdn.microsoft.com/2E7FB4DA-88AD-4739-ACE0-D43670F914D4">CLUSTER_ENUM_ITEM</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 


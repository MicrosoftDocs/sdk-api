---
UID: NC:clusapi.PCLUSAPI_CLUSTER_ENUM_EX
title: PCLUSAPI_CLUSTER_ENUM_EX
author: windows-driver-content
description: Enumerates the objects in a cluster, and then gets the name and properties of the cluster object.
old-location: mscs\clusterenumex.htm
old-project: MsCS
ms.assetid: F50FB801-8ACA-40BD-9E89-7E3AF2CA2DA5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PCLUSAPI_CLUSTER_ENUM_EX, PCLUSAPI_CLUSTER_ENUM_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_ENUM_EX, mscs.clusterenumex
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_ENUM_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_ENUM_EX callback


## -description


Enumerates the objects in a cluster, and then gets the name and properties of the cluster object.


## -parameters




### -param hClusterEnum [in]

A handle to the enumerator that is returned by the <a href="https://msdn.microsoft.com/DA35A67E-6F20-47CC-A96A-591702A79EF5">ClusterOpenEnumEx</a> function.


### -param dwIndex [in]

The index that identifies the next cluster object to enumerate. This parameter should be zero for the first call to the  <i>ClusterEnumEx</i>  function and then be  incremented for subsequent calls.


### -param pItem [in, out]

A pointer that receives the returned cluster object properties.


### -param cbItem [in, out]

On input, the size of the  <i>pItem</i>   parameter.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes that are  written into the buffer.


## -returns





Returns DWORD that ...






## -see-also




<a href="https://msdn.microsoft.com/2E7FB4DA-88AD-4739-ACE0-D43670F914D4">CLUSTER_ENUM_ITEM</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 


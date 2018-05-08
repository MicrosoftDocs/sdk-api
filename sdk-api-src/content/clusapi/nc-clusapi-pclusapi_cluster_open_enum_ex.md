---
UID: NC:clusapi.PCLUSAPI_CLUSTER_OPEN_ENUM_EX
title: PCLUSAPI_CLUSTER_OPEN_ENUM_EX
author: windows-driver-content
description: Opens a handle to a cluster in order to iterate through its objects.
old-location: mscs\clusteropenenumex.htm
old-project: MsCS
ms.assetid: DA35A67E-6F20-47CC-A96A-591702A79EF5
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_CLUSTER_OPEN_ENUM_EX, PCLUSAPI_CLUSTER_OPEN_ENUM_EX callback, PCLUSAPI_CLUSTER_OPEN_ENUM_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_OPEN_ENUM_EX, mscs.clusteropenenumex
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
-	kbSyntax
api_type:
-	<TBD>
api_location:
-
api_name:
-	PCLUSAPI_CLUSTER_OPEN_ENUM_EX callback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_OPEN_ENUM_EX callback function


## -description


Opens a handle to a cluster  in order to    iterate through its objects.


## -parameters




### -param hCluster [in]

The handle to the cluster.


### -param dwType [in]

A bitmask that describes the type of objects to be enumerated. This must be one or more of the 
       <a href="https://msdn.microsoft.com/e3d5a207-d30e-4935-be95-0957e68d4fe6">CLUSTER_ENUM</a> enumeration values.


### -param pOptions [in, optional]

TBD


## -returns



If the operation succeeds, returns a handle to a cluster enumerator.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the function <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/e3d5a207-d30e-4935-be95-0957e68d4fe6">CLUSTER_ENUM</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 


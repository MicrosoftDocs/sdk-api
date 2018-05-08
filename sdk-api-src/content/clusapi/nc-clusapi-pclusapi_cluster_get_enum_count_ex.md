---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX
title: PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX
author: windows-driver-content
description: Returns the number of cluster objects that are associated with a cluster enumeration handle.
old-location: mscs\clustergetenumcountex.htm
old-project: MsCS
ms.assetid: EC66C1CF-4CAA-41C6-ABA1-BB576F0293F4
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX callback, PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX, mscs.clustergetenumcountex
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
-	PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX callback function


## -description


Returns the 
    number of cluster objects that are associated with a 
    cluster enumeration handle.


## -parameters




### -param hClusterEnum [in]

The handle to a cluster enumeration. This handle is obtained from the  
      <a href="https://msdn.microsoft.com/DA35A67E-6F20-47CC-A96A-591702A79EF5">ClusterOpenEnumEx</a>    function. A valid handle is required. This 
      parameter cannot be NULL.


## -returns



The number of 
       objects that are associated with the enumeration handle.




## -see-also




<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 


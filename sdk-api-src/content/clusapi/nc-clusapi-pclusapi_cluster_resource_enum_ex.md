---
UID: NC:clusapi.PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX
title: PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX
author: windows-driver-content
description: Enumerates a resource and then returns a pointer to the current dependent resource or node.
old-location: mscs\clusterresourceenumex.htm
old-project: MsCS
ms.assetid: 9B5C03DF-84BB-4B3A-8404-94C64F192305
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX callback, PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX, mscs.clusterresourceenumex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
-	PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX callback function


## -description


Enumerates a resource and then returns a pointer to the current  dependent resource or node.


## -parameters




### -param hResourceEnumEx [in]

A handle to a resource enumeration   that is returned from 
       the <a href="https://msdn.microsoft.com/B43460F1-4BFE-48E0-889A-56370320E4E6">ClusterResourceOpenEnumEx</a> function.


### -param dwIndex [in]

The index of the resource or node object to return. This parameter should be zero for the first call to the 
       <i>ClusterResourceEnumEx</i> function and then be  
       incremented for subsequent calls.


### -param pItem [in, out]

A pointer that receives the returned object.


### -param cbItem [in, out]

On input, the size of the  <i>pItem</i> parameter.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes written into the buffer.


## -returns



The function returns one of the following values.




## -see-also




<a href="https://msdn.microsoft.com/B43460F1-4BFE-48E0-889A-56370320E4E6">ClusterResourceOpenEnumEx</a>



<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 


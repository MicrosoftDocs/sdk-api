---
UID: NC:clusapi.PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX
title: PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX
author: windows-sdk-content
description: Enumerates a resource and then returns a pointer to the current dependent resource or node.
old-location: mscs\clusterresourceenumex.htm
old-project: mscs
ms.assetid: 9B5C03DF-84BB-4B3A-8404-94C64F192305
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusterResourceEnumEx, ClusterResourceEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX function [Failover Cluster], clusapi/ClusterResourceEnumEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX, mscs.clusterresourceenumex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceEnumEx
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
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
       <b>ClusterResourceEnumEx</b> function and then be  
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
 

 


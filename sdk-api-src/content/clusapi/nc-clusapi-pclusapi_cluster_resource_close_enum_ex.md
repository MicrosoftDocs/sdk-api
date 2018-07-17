---
UID: NC:clusapi.PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX
title: PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX
author: windows-sdk-content
description: Closes a handle to a resource enumeration.
old-location: mscs\clusterresourcecloseenumex.htm
old-project: mscs
ms.assetid: 643CA960-F4F1-4028-B0A3-5258E9421D62
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusterResourceCloseEnumEx, ClusterResourceCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterResourceCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, mscs.clusterresourcecloseenumex
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
 - ClusterResourceCloseEnumEx
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX callback function


## -description


Closes a handle to a  resource enumeration.


## -parameters




### -param hResourceEnumEx [in]

The handle to a resource enumeration  to  close.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a different <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 


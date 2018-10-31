---
UID: NF:clusapi.ClusterResourceCloseEnumEx
title: ClusterResourceCloseEnumEx function
author: windows-sdk-content
description: Closes a handle to a resource enumeration.
old-location: mscs\clusterresourcecloseenumex.htm
tech.root: mscs
ms.assetid: 643CA960-F4F1-4028-B0A3-5258E9421D62
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ClusterResourceCloseEnumEx, ClusterResourceCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterResourceCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, mscs.clusterresourcecloseenumex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceCloseEnumEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceCloseEnumEx function


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




<a href="https://msdn.microsoft.com/en-us/library/Aa372262(v=VS.85).aspx">Failover Cluster Resource Management Functions</a>
 

 


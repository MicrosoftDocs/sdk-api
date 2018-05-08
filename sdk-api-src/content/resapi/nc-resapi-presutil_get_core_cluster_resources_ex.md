---
UID: NC:resapi.PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX
title: PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX
author: windows-driver-content
description: Returns handles to the core, &#32;Network Name, IP Address, and quorum resources. The PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX type defines a pointer to this function.
old-location: mscs\resutilgetcoreclusterresourcesex.htm
old-project: MsCS
ms.assetid: F6C576C1-5D34-41EB-95A4-BC8F78F02414
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX, PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX callback, PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX callback function [Failover Cluster], mscs.resutilgetcoreclusterresourcesex, resapi/PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX callback function


## -description


Returns handles to the 
    <a href="https://msdn.microsoft.com/46b71882-be37-4c3f-a328-a394c1310958">core</a>,  <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a>, 
    <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a>,  and 
    <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum</a> resources. The <b>PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX</b> type defines a pointer to this function.


## -parameters




### -param hClusterIn


### -param *phClusterNameResourceOut


### -param *phClusterIPAddressResourceOut


### -param *phClusterQuorumResourceOut


### -param dwDesiredAccess [in]

The requested access privileges. This  might be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or M<b>AXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0), an undefined error  might be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="https://msdn.microsoft.com/cadfeaf7-951f-4fc7-96fa-2e256e52a370">ResUtilGetCoreClusterResources</a>.


#### - hCluster [in]

The cluster handle (see <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>).


#### - phClusterIPAddressResource [out]

Not used.


#### - phClusterNameResource [out]

A pointer to a resource handle to the core 
      <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource for the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>, which stores the cluster name.


#### - phClusterQuorumResource [out]

A pointer to a resource handle to the cluster's 
      <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 


---
UID: NF:resapi.ResUtilGetCoreClusterResourcesEx
title: ResUtilGetCoreClusterResourcesEx function
author: windows-sdk-content
description: Returns handles to the core, &#32;Network Name, IP Address, and quorum resources. The PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX type defines a pointer to this function.
old-location: mscs\resutilgetcoreclusterresourcesex.htm
tech.root: mscs
ms.assetid: F6C576C1-5D34-41EB-95A4-BC8F78F02414
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX, PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX function [Failover Cluster], ResUtilGetCoreClusterResourcesEx, ResUtilGetCoreClusterResourcesEx function [Failover Cluster], mscs.resutilgetcoreclusterresourcesex, resapi/PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX, resapi/ResUtilGetCoreClusterResourcesEx
ms.topic: function
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
 - ext-ms-win-cluster-resutils-l1-1-0.dll
 - ext-ms-win-cluster-resutils-l1-1-1.dll
api_name:
 - ResUtilGetCoreClusterResourcesEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetCoreClusterResourcesEx function


## -description


Returns handles to the 
    <a href="https://msdn.microsoft.com/46b71882-be37-4c3f-a328-a394c1310958">core</a>,  <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a>, 
    <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a>,  and 
    <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum</a> resources. The <b>PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX</b> type defines a pointer to this function.


## -parameters




### -param hClusterIn [in]

The cluster handle (see <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>).


### -param phClusterNameResourceOut [out]

A pointer to a resource handle to the core 
      <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource for the 
      <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>, which stores the cluster name.


### -param phClusterQuorumResourceOut [out]

Not used.


### -param dwDesiredAccess [in]

The requested access privileges. This  might be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or M<b>AXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0), an undefined error  might be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="https://msdn.microsoft.com/cadfeaf7-951f-4fc7-96fa-2e256e52a370">ResUtilGetCoreClusterResources</a>.


#### - phClusterQuorumResource [out]

A pointer to a resource handle to the cluster's 
      <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 


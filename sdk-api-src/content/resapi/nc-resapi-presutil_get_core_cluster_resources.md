---
UID: NC:resapi.PRESUTIL_GET_CORE_CLUSTER_RESOURCES
title: PRESUTIL_GET_CORE_CLUSTER_RESOURCES
author: windows-sdk-content
description: Returns handles to the core&#32;Network Name, IP Address and quorum resources. The PRESUTIL_GET_CORE_CLUSTER_RESOURCES type defines a pointer to this function.
old-location: mscs\resutilgetcoreclusterresources.htm
old-project: MsCS
ms.assetid: cadfeaf7-951f-4fc7-96fa-2e256e52a370
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRESUTIL_GET_CORE_CLUSTER_RESOURCES, PRESUTIL_GET_CORE_CLUSTER_RESOURCES callback, PRESUTIL_GET_CORE_CLUSTER_RESOURCES callback function [Failover Cluster], _wolf_resutilgetcoreclusterresources, mscs.resutilgetcoreclusterresources, resapi/PRESUTIL_GET_CORE_CLUSTER_RESOURCES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_GET_CORE_CLUSTER_RESOURCES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PRESUTIL_GET_CORE_CLUSTER_RESOURCES callback function


## -description


Returns handles to the 
    <a href="https://msdn.microsoft.com/46b71882-be37-4c3f-a328-a394c1310958">core</a> <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a>, 
    <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a> and 
    <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum</a> resources. The <b>PRESUTIL_GET_CORE_CLUSTER_RESOURCES</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Cluster handle (see <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>).


### -param *phClusterNameResource [out]

Pointer to a resource handle to the core 
      <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource for the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>, which stores the cluster name.


### -param *phClusterIPAddressResource [out]

Not used.


### -param *phClusterQuorumResource [out]

Pointer to a resource handle to the cluster's 
      <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 


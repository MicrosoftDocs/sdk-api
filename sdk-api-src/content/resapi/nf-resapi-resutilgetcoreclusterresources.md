---
UID: NF:resapi.ResUtilGetCoreClusterResources
title: ResUtilGetCoreClusterResources function (resapi.h)
author: windows-sdk-content
description: Returns handles to the core&#32;Network Name, IP Address and quorum resources. The PRESUTIL_GET_CORE_CLUSTER_RESOURCES type defines a pointer to this function.
old-location: mscs\resutilgetcoreclusterresources.htm
tech.root: MsCS
ms.assetid: cadfeaf7-951f-4fc7-96fa-2e256e52a370
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_CORE_CLUSTER_RESOURCES, PRESUTIL_GET_CORE_CLUSTER_RESOURCES function [Failover Cluster], ResUtilGetCoreClusterResources, ResUtilGetCoreClusterResources function [Failover Cluster], _wolf_resutilgetcoreclusterresources, mscs.resutilgetcoreclusterresources, resapi/PRESUTIL_GET_CORE_CLUSTER_RESOURCES, resapi/ResUtilGetCoreClusterResources
ms.topic: function
f1_keywords: 
 - "resapi/ResUtilGetCoreClusterResources"
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
req.lib: ResUtils.lib
req.dll: ResUtils.Dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.Dll
 - Ext-MS-Win-Cluster-ResUtils-l1-1-0.dll
 - ext-ms-win-cluster-resutils-l1-1-1.dll
api_name:
 - ResUtilGetCoreClusterResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResUtilGetCoreClusterResources function


## -description


Returns handles to the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/core-resources">core</a> <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/network-name">Network Name</a>, 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/ip-address">IP Address</a> and 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/quorum-resource">quorum</a> resources. The <b>PRESUTIL_GET_CORE_CLUSTER_RESOURCES</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Cluster handle (see <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>).


### -param phClusterNameResource [out]

Pointer to a resource handle to the core 
      <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resource for the 
      <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster</a>, which stores the cluster name.


### -param phClusterIPAddressResource [out]

Not used.


### -param phClusterQuorumResource [out]

Pointer to a resource handle to the cluster's 
      <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a>.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>
 

 


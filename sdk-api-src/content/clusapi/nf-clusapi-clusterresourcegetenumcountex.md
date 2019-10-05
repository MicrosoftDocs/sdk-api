---
UID: NF:clusapi.ClusterResourceGetEnumCountEx
title: ClusterResourceGetEnumCountEx function (clusapi.h)
author: windows-sdk-content
description: Returns the number of cluster objects that are associated with a resource enumeration handle.
old-location: mscs\clusterresourcegetenumcountex.htm
tech.root: MsCS
ms.assetid: 97C22642-F968-4E41-90BC-28DF8DF5886C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClusterResourceGetEnumCountEx, ClusterResourceGetEnumCountEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX function [Failover Cluster], clusapi/ClusterResourceGetEnumCountEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX, mscs.clusterresourcegetenumcountex
ms.topic: function
f1_keywords: 
 - "clusapi/ClusterResourceGetEnumCountEx"
dev_langs:
 - c++
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
api_name:
 - ClusterResourceGetEnumCountEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterResourceGetEnumCountEx function


## -description


Returns the number of  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a>  that are associated with a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resources">resource</a> enumeration handle.


## -parameters




### -param hResourceEnumEx [in]

The handle to a resource enumeration. This handle is obtained from 
the <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenumex">ClusterResourceOpenEnumEx</a> function. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



The number of objects that are associated with the enumeration handle.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenumex">ClusterResourceOpenEnumEx</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>
 

 


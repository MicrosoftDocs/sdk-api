---
UID: NF:clusapi.ClusterResourceTypeCloseEnum
title: ClusterResourceTypeCloseEnum function (clusapi.h)
author: windows-sdk-content
description: Closes a resource type enumeration handle.
old-location: mscs\clusterresourcetypecloseenum.htm
tech.root: MsCS
ms.assetid: c6524604-7a73-414c-95bb-dce9524f3295
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClusterResourceTypeCloseEnum, ClusterResourceTypeCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM function [Failover Cluster], _wolf_clusterresourcetypecloseenum, clusapi/ClusterResourceTypeCloseEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM, mscs.clusterresourcetypecloseenum
ms.topic: function
f1_keywords: 
 - "clusapi/ClusterResourceTypeCloseEnum"
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - ClusterResourceTypeCloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterResourceTypeCloseEnum function


## -description


Closes a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-types">resource type</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hResTypeEnum [in]

Enumeration handle to be closed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeenum">ClusterResourceTypeEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeopenenum">ClusterResourceTypeOpenEnum</a>
 

 


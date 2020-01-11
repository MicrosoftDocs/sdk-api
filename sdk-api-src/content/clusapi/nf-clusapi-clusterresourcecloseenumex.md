---
UID: NF:clusapi.ClusterResourceCloseEnumEx
title: ClusterResourceCloseEnumEx function (clusapi.h)
description: Closes a handle to a resource enumeration.
old-location: mscs\clusterresourcecloseenumex.htm
tech.root: MsCS
ms.assetid: 643CA960-F4F1-4028-B0A3-5258E9421D62
ms.date: 12/05/2018
ms.keywords: ClusterResourceCloseEnumEx, ClusterResourceCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterResourceCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, mscs.clusterresourcecloseenumex
f1_keywords:
- clusapi/ClusterResourceCloseEnumEx
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
- Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
- Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
- Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
- ClusterResourceCloseEnumEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
the function returns a different <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>
 

 


---
UID: NF:clusapi.ClusterResourceCloseEnumEx
title: ClusterResourceCloseEnumEx function (clusapi.h)
description: Closes a handle to a resource enumeration.
helpviewer_keywords: ["ClusterResourceCloseEnumEx","ClusterResourceCloseEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX","PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX function [Failover Cluster]","clusapi/ClusterResourceCloseEnumEx","clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX","mscs.clusterresourcecloseenumex"]
old-location: mscs\clusterresourcecloseenumex.htm
tech.root: MsCS
ms.assetid: 643CA960-F4F1-4028-B0A3-5258E9421D62
ms.date: 12/05/2018
ms.keywords: ClusterResourceCloseEnumEx, ClusterResourceCloseEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX function [Failover Cluster], clusapi/ClusterResourceCloseEnumEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM_EX, mscs.clusterresourcecloseenumex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterResourceCloseEnumEx
 - clusapi/ClusterResourceCloseEnumEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceCloseEnumEx
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
the function returns a different <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>
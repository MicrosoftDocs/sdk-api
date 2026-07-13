---
UID: NF:clusapi.ClusterResourceOpenEnumEx
title: ClusterResourceOpenEnumEx function (clusapi.h)
description: Opens a handle to a resource enumeration that enables iteration through a resource's dependencies and nodes.
helpviewer_keywords: ["ClusterResourceOpenEnumEx","ClusterResourceOpenEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX","PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX function [Failover Cluster]","clusapi/ClusterResourceOpenEnumEx","clusapi/PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX","mscs.clusterresourceopenenumex"]
old-location: mscs\clusterresourceopenenumex.htm
tech.root: MsCS
ms.assetid: B43460F1-4BFE-48E0-889A-56370320E4E6
ms.date: 12/05/2018
ms.keywords: ClusterResourceOpenEnumEx, ClusterResourceOpenEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX function [Failover Cluster], clusapi/ClusterResourceOpenEnumEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX, mscs.clusterresourceopenenumex
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
 - ClusterResourceOpenEnumEx
 - clusapi/ClusterResourceOpenEnumEx
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
 - ClusterResourceOpenEnumEx
---

# ClusterResourceOpenEnumEx function


## -description

Opens a handle to a  resource enumeration  that  enables iteration   through a resource's dependencies and nodes.

## -parameters

### -param hCluster [in]

A handle to the resource to iterate through.

### -param lpszProperties [in, optional]

A pointer to a list of names of common properties.

### -param cbProperties [in]

The size, in bytes, of the <i>lpszProperties</i>  parameter.

### -param lpszRoProperties [in, optional]

A pointer to a list of names of read-only common properties.

### -param cbRoProperties [in]

The size, in bytes, of the <i>lpszRoProperties</i>  parameter.

### -param dwFlags [in]

The index that identifies the next object to enumerate. This parameter should be zero for the first call to <b>ClusterResourceOpenEnumEx</b> and then be incremented for subsequent calls.

## -returns

If the operation succeeds, the function returns an enumeration handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>
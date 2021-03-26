---
UID: NF:clusapi.ClusterOpenEnumEx
title: ClusterOpenEnumEx function (clusapi.h)
description: Opens a handle to a cluster in order to iterate through its objects.
helpviewer_keywords: ["ClusterOpenEnumEx","ClusterOpenEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_OPEN_ENUM_EX","PCLUSAPI_CLUSTER_OPEN_ENUM_EX function [Failover Cluster]","clusapi/ClusterOpenEnumEx","clusapi/PCLUSAPI_CLUSTER_OPEN_ENUM_EX","mscs.clusteropenenumex"]
old-location: mscs\clusteropenenumex.htm
tech.root: MsCS
ms.assetid: DA35A67E-6F20-47CC-A96A-591702A79EF5
ms.date: 12/05/2018
ms.keywords: ClusterOpenEnumEx, ClusterOpenEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_OPEN_ENUM_EX, PCLUSAPI_CLUSTER_OPEN_ENUM_EX function [Failover Cluster], clusapi/ClusterOpenEnumEx, clusapi/PCLUSAPI_CLUSTER_OPEN_ENUM_EX, mscs.clusteropenenumex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
 - ClusterOpenEnumEx
 - clusapi/ClusterOpenEnumEx
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - ClusterOpenEnumEx
---

# ClusterOpenEnumEx function


## -description

Opens a handle to a cluster  in order to    iterate through its objects.

## -parameters

### -param hCluster [in]

The handle to the cluster.

### -param dwType [in]

A bitmask that describes the type of objects to be enumerated. This must be one or more of the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_enum">CLUSTER_ENUM</a> enumeration values.

### -param pOptions [in, optional] [in, optional]

Options.

## -returns

If the operation succeeds, returns a handle to a cluster enumerator.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the function <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_enum">CLUSTER_ENUM</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Function</a>